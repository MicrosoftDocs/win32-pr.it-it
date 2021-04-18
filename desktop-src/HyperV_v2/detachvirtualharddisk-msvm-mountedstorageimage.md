---
description: Scollega l'immagine di archiviazione montata associata a questa classe.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Metodo DetachVirtualHardDisk della classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315503"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="be6dd-103">Metodo DetachVirtualHardDisk della classe MSVM \_ MountedStorageImage</span><span class="sxs-lookup"><span data-stu-id="be6dd-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="be6dd-104">Scollega l'immagine di archiviazione montata associata a questa classe.</span><span class="sxs-lookup"><span data-stu-id="be6dd-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be6dd-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="be6dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be6dd-106">Parameters</span></span>

<span data-ttu-id="be6dd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="be6dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be6dd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be6dd-108">Return value</span></span>

<span data-ttu-id="be6dd-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be6dd-109">Type: **uint32**</span></span>

<span data-ttu-id="be6dd-110">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="be6dd-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="be6dd-111">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="be6dd-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be6dd-112">**Non riuscito** (1)</span><span class="sxs-lookup"><span data-stu-id="be6dd-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="be6dd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="be6dd-113">Remarks</span></span>

<span data-ttu-id="be6dd-114">L'accesso alla [**classe \_ MountedStorageImage di MSVM**](msvm-mountedstorageimage.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="be6dd-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="be6dd-115">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="be6dd-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="be6dd-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="be6dd-116">Examples</span></span>

<span data-ttu-id="be6dd-117">Nell'esempio C# riportato di seguito viene illustrato come scollegare un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="be6dd-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="be6dd-118">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="be6dd-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="be6dd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be6dd-119">Requirements</span></span>



| <span data-ttu-id="be6dd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="be6dd-120">Requirement</span></span> | <span data-ttu-id="be6dd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="be6dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6dd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be6dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be6dd-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be6dd-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be6dd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be6dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be6dd-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be6dd-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be6dd-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="be6dd-126">Namespace</span></span><br/>                | <span data-ttu-id="be6dd-127">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="be6dd-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be6dd-128">MOF</span><span class="sxs-lookup"><span data-stu-id="be6dd-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be6dd-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be6dd-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be6dd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be6dd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be6dd-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be6dd-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be6dd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be6dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6dd-133">**\_MountedStorageImage MSVM**</span><span class="sxs-lookup"><span data-stu-id="be6dd-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

