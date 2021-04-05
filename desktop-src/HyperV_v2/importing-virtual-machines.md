---
description: Nell'esempio C# riportato di seguito viene illustrato come utilizzare il metodo MigrateVirtualSystemToHost per eseguire una semplice migrazione di una macchina virtuale.
ms.assetid: A3E4AAA2-3AE6-4D7D-8D7B-1ED367D398C0
title: Migrazione di macchine virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4446830b61e2fabb79d0938520d0b503da167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754242"
---
# <a name="migrating-virtual-machines"></a><span data-ttu-id="f74fd-103">Migrazione di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="f74fd-103">Migrating virtual machines</span></span>

<span data-ttu-id="f74fd-104">Nell'esempio C# riportato di seguito viene illustrato come utilizzare il metodo [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) per eseguire una semplice migrazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f74fd-104">The following C# sample demonstrates how to use the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) method to perform a simple migration of a virtual machine.</span></span> <span data-ttu-id="f74fd-105">In questo esempio vengono utilizzati i pool di risorse per ottenere i percorsi VHD corretti.</span><span class="sxs-lookup"><span data-stu-id="f74fd-105">This example uses resource pools to obtain the correct VHD paths.</span></span> <span data-ttu-id="f74fd-106">Questo codice è tratto dall' [esempio di migrazione delle macchine virtuali Hyper-V](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Hyper-V%20virtual%20machine%20migration%20sample).</span><span class="sxs-lookup"><span data-stu-id="f74fd-106">This code is taken from the [Hyper-V virtual machine migration sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Hyper-V%20virtual%20machine%20migration%20sample).</span></span>

<span data-ttu-id="f74fd-107">La sintassi della riga di comando per eseguire questo esempio è:</span><span class="sxs-lookup"><span data-stu-id="f74fd-107">The command-line syntax to run this sample is:</span></span>

<span data-ttu-id="f74fd-108">**MigrationSamples.exe VM-and-Storage-Simple** *SourceHost* *DestinationHost* *VmName*</span><span class="sxs-lookup"><span data-stu-id="f74fd-108">**MigrationSamples.exe vm-and-storage-simple** *SourceHost* *DestinationHost* *VmName*</span></span>

<span data-ttu-id="f74fd-109">dove i parametri sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f74fd-109">where the parameters are as follows:</span></span>

-   <span data-ttu-id="f74fd-110">*SourceHost* è il nome dell'host corrente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f74fd-110">*SourceHost* is the name of the current host of the virtual machine.</span></span>
-   <span data-ttu-id="f74fd-111">*DestinationHost* è il nome dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f74fd-111">*DestinationHost* is the name of the destination host.</span></span>
-   <span data-ttu-id="f74fd-112">*VmName* è il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f74fd-112">*VmName* is the name of the virtual machine.</span></span>


```CSharp
/// <summary>
/// Migrates a VM without any modification, using all defaults.
/// Resource pools will be used to get correct path for the VHDs.
/// </summary>
/// <param name="sourceHost">Migration source hostname</param>
/// <param name="destinationHost">
/// Migration destination hostname
/// </param>
/// <param name="vmName">VM name.</param>
public
void
VmAndStorageMigrationSimple(
    string sourceHost,
    string destinationHost,
    string vmName
    )
{
    ManagementScope srcScope = new ManagementScope(
        @"\\" + sourceHost + @"\root\virtualization\v2", null);

    using (ManagementObject migrationSettingData = GetMigrationSettingData(srcScope))
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, srcScope))
    {
        migrationSettingData["MigrationType"] = MigrationType.VirtualSystemAndStorage;
        migrationSettingData["TransportType"] = TransportType.TCP;

        // Get the VHD SASDs
        string[] sasds = null;
        ManagementObject[] vhdList = WmiUtilities.GetVhdSettings(vm);
        if (vhdList != null)
        {
            sasds = new string[vhdList.Length];

            for (uint index = 0; index < vhdList.Length; ++index)
            {
                using (ManagementObject vhd = vhdList[index])
                {
                    // Change the VHD path to an empty string which will force
                    // the system to use resource pools to get the right path at
                    // the destination node.
                    vhd["HostResource"] = new string[] { "" };

                    // Create array of embedded instances.
                    sasds[index] = vhd.GetText(TextFormat.CimDtd20);
                }
            }
        }
        else
        {
            Console.WriteLine("No VHDs found associated with the VM. Skipping VHDs...");
        }

        // Perform migration.
        Console.WriteLine("Performing migration...");
        Migrate(srcScope,
            vmName,
            destinationHost,
            migrationSettingData.GetText(TextFormat.CimDtd20),
            null,
            sasds);
    }
}
```



<span data-ttu-id="f74fd-113">Il codice C# seguente contiene l'implementazione della maggior parte dei metodi di utilità chiamati dall'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="f74fd-113">The following C# code contains the implementation of most of the utility methods called from the example above.</span></span>


```CSharp
class MigrationCommon
{
    ///////////////////////////////////////////////////////////////////////
    // Common values and methods for all migration types.
    ///////////////////////////////////////////////////////////////////////

    /// <summary>
    /// Defines the migration types.
    /// </summary>
    public enum MigrationType
    {
        VirtualSystem = 32768,
        Storage = 32769,
        Staged = 32770,
        VirtualSystemAndStorage = 32771
    };

    /// <summary>
    /// Defines migration transport types.
    /// </summary>
    public enum TransportType
    {
        TCP = 5
    };

    /// <summary>
    /// Gets the virtual system migration service.
    /// </summary>
    /// <param name="scope">The scope to use when connecting to WMI.</param>
    /// <returns>The virtual system migration service.</returns>
    public
    ManagementObject
    GetVirtualMachineMigrationService(
        ManagementScope scope)
    {
        using (ManagementClass migrationServiceClass = new ManagementClass("Msvm_VirtualSystemMigrationService"))
        {
            migrationServiceClass.Scope = scope;

            ManagementObject migrationService =
                WmiUtilities.GetFirstObjectFromCollection(migrationServiceClass.GetInstances());

            return migrationService;
        }
    }

    /// <summary>
    /// Returns the instance of
    /// Msvm_VirtualSystemMigrationServiceSettingData
    /// associated with the service.
    /// </summary>
    /// <param name="service">Migration service instance</param>
    /// <returns>
    /// Instance of Msvm_VirtualSystemMigrationServiceSettingData
    /// </returns>
    public
    ManagementObject
    GetMigrationServiceSettings(
        ManagementObject service
        )
    {
        ManagementObject serviceSetting = null;
        using (ManagementObjectCollection settingCollection =
            service.GetRelated("Msvm_VirtualSystemMigrationServiceSettingData"))
        {
            foreach (ManagementObject mgmtObj in settingCollection)
            {
                serviceSetting = mgmtObj;
                break;
            }
        }

        return serviceSetting;
    }

    /// <summary>
    /// Retuns the migration setting data object to be used for
    /// migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <returns>Migration setting data object</returns>
    public
    ManagementObject
    GetMigrationSettingData(
        ManagementScope scope
        )
    {
        ManagementObject migrationSettingData = null;
        ManagementPath settingPath =
            new ManagementPath("Msvm_VirtualSystemMigrationSettingData");

        using (ManagementClass migrationSettingDataClass = new ManagementClass(scope, settingPath, null))
        {
            migrationSettingData = migrationSettingDataClass.CreateInstance();
        }

        return migrationSettingData;
    }

    /// <summary>
    /// Performs the migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    public
    void
    Migrate(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams = service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("MigrateVirtualSystemToHost", inParams, null))
            {
                WmiUtilities.ValidateOutput(outParams, scope);
            }
        }
    }

    /// <summary>
    /// Performs migratability check.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    /// <returns>true if virtual machine is migratable, false otherwise</returns>
    public
    bool
    CheckMigratability(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams =
            service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("CheckVirtualSystemIsMigratable", inParams, null))
            {
                return WmiUtilities.ValidateOutput(outParams, scope, false, true);
            }
        }
    }

    /// <summary>
    /// Returns array of IP addresses on which the migration destination
    /// host is listening for incoming VM migration request.
    /// </summary>
    /// <param name="destinationHost">
    /// Migration destination hostname
    /// </param>
    /// <returns>Listening IP addresses</returns>
    public
    string[]
    GetMigrationDestinationListenAddresses(
        string destinationHost
        )
    {
        string[] ipAddresses = null;

        ManagementScope scope = new ManagementScope(
            @"\\" + destinationHost + @"\root\virtualization\v2", null);

        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementObject serviceSetting = GetMigrationServiceSettings(service))
        {
            if (!((bool)serviceSetting["EnableVirtualSystemMigration"]))
            {
                throw new Exception("Destination host does not " +
                    "allow VM migration");
            }

            ipAddresses =
                (string[])service["MigrationServiceListenerIPAddressList"];
            if (ipAddresses == null)
            {
                throw new Exception("Destination host does not have " +
                    "networks set for VM migration");
            }
        }

        return ipAddresses;
    }
}
```



 

 



