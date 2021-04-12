---
description: Wmiadap è un'applicazione eseguita in Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233976"
---
# <a name="wmiadap"></a><span data-ttu-id="466aa-103">wmiadap</span><span class="sxs-lookup"><span data-stu-id="466aa-103">wmiadap</span></span>

<span data-ttu-id="466aa-104">Wmiadap è un'applicazione eseguita in Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="466aa-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="466aa-105">In genere, questo consente agli sviluppatori e agli amministratori IT di creare script che accedono alle informazioni sulle prestazioni, ad esempio la quantità di memoria usata da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="466aa-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="466aa-106">Nell'argomento seguente viene descritta l'interfaccia della riga di comando che è possibile utilizzare per controllare il modo in cui wmiadap recupera le informazioni.</span><span class="sxs-lookup"><span data-stu-id="466aa-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="466aa-107">Wmiadap viene installato con il sistema operativo nella maggior parte dei sistemi, nella directory C: \\ Windows \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="466aa-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="466aa-108">Se vengono visualizzati messaggi di errore relativi wmiadap.exe, cercare [supporto tecnico Microsoft](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="466aa-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="466aa-109">In genere, non è consigliabile eliminare wmiadap.exe dal sistema, se non diversamente indicato.</span><span class="sxs-lookup"><span data-stu-id="466aa-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="466aa-110">Il trasferimento dei dati dalle librerie di prestazioni e l'aggiornamento delle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) vengono eseguiti dai provider [wmiperfclass](wmi-providers.md) e [wmiperfinst](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="466aa-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="466aa-111">Il provider WmiPerfClass Aggiorna [le classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI solo quando viene aggiunto un nuovo oggetto prestazioni.</span><span class="sxs-lookup"><span data-stu-id="466aa-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="466aa-112">È comunque possibile eseguire wmiadap con l'opzione **/r** per analizzare i driver Windows Driver Model per creare gli oggetti prestazioni.</span><span class="sxs-lookup"><span data-stu-id="466aa-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="466aa-113">L'opzione **/f** forza ancora un aggiornamento delle classi WMI dalle librerie delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="466aa-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="466aa-114">Al prompt dei comandi sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="466aa-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="466aa-115">**wmiadap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="466aa-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="466aa-116">Commutatori</span><span class="sxs-lookup"><span data-stu-id="466aa-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="466aa-117"><span id="_f"></span><span id="_F"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="466aa-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="466aa-118">Analizza tutte le librerie di prestazioni nel sistema e aggiorna le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="466aa-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="466aa-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="466aa-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="466aa-120">Analizza tutti i driver Windows Driver Model nel sistema per creare gli oggetti prestazioni.</span><span class="sxs-lookup"><span data-stu-id="466aa-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="466aa-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="466aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="466aa-122">Librerie di prestazioni e WMI</span><span class="sxs-lookup"><span data-stu-id="466aa-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="466aa-123">**winmgmt**</span><span class="sxs-lookup"><span data-stu-id="466aa-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
