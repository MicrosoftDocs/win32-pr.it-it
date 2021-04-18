---
description: È possibile nascondere il pulsante Annulla usato per annullare un'installazione usando un'opzione della riga di comando, l'API Windows Installer o un'azione personalizzata. Il pulsante Annulla può essere nascosto per una parte o per tutte le installazioni a seconda del metodo usato.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Nascondere il pulsante Annulla durante un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314256"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="a2ed8-104">Nascondere il pulsante Annulla durante un'installazione</span><span class="sxs-lookup"><span data-stu-id="a2ed8-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="a2ed8-105">È possibile nascondere il pulsante **Annulla** usato per annullare un'installazione usando un'opzione della riga di comando, l'API Windows Installer o un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="a2ed8-106">Il pulsante **Annulla** può essere nascosto per una parte o per tutte le installazioni a seconda del metodo usato.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="a2ed8-107">Nascondere il pulsante Annulla dalla riga di comando</span><span class="sxs-lookup"><span data-stu-id="a2ed8-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="a2ed8-108">Il pulsante **Annulla** può essere nascosto durante l'installazione tramite l'opzione della riga di comando (!).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="a2ed8-109">Questa operazione può essere eseguita solo per un'installazione di base a livello di interfaccia utente (/QB).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="a2ed8-110">Il pulsante **Annulla** è nascosto per l'intera installazione.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="a2ed8-111">Per altre informazioni, vedere [Opzioni della riga di comando](command-line-options.md) e [livelli dell'interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="a2ed8-112">La riga di comando seguente nasconde il pulsante **Annulla** e installa Example.msi.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="a2ed8-113">**msiexec/I example.msi/QB!**</span><span class="sxs-lookup"><span data-stu-id="a2ed8-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="a2ed8-114">Nascondere il pulsante Annulla da un'applicazione o da uno script</span><span class="sxs-lookup"><span data-stu-id="a2ed8-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="a2ed8-115">È possibile scrivere un'applicazione o uno script per nascondere il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="a2ed8-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="a2ed8-116">Questa operazione può essere eseguita solo per un'installazione a livello di interfaccia utente di base, in modo che il pulsante **Annulla** sia nascosto per l'intera installazione.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="a2ed8-117">Per nascondere il pulsante Annulla da un'applicazione, impostare INSTALLUILEVEL \_ HIDECANCEL quando si chiama [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="a2ed8-118">Nell'esempio seguente viene nascosto il pulsante **Annulla** e viene installato Example.msi.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



<span data-ttu-id="a2ed8-119">Per nascondere il pulsante **Annulla** dallo script, aggiungere msiUILevelHideCancel alla proprietà [**UILevel**](installer-uilevel.md) dell' [**oggetto Installer**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="a2ed8-120">Nell'esempio VBScript seguente viene nascosto il pulsante **Annulla** e viene installato Example.msi.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="a2ed8-121">Nascondere il pulsante Annulla per parti di un'installazione mediante un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="a2ed8-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="a2ed8-122">L'installazione può nascondere e scoprire il pulsante **Annulla** durante le parti di un'installazione inviando un \_ messaggio INSTALLMESSAGE COMMONDATA utilizzando un'azione o script personalizzati della dll.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="a2ed8-123">Per altre informazioni, vedere [librerie a collegamento dinamico](dynamic-link-libraries.md), [script](scripts.md), [azioni personalizzate](custom-actions.md)e [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a2ed8-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="a2ed8-124">Una chiamata a un'azione personalizzata deve fornire un record.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="a2ed8-125">Il campo 1 di questo record deve contenere il valore 2 (due) per specificare il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="a2ed8-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="a2ed8-126">Il campo 2 deve contenere il valore 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="a2ed8-127">Il valore 0 nel campo 2 nasconde il pulsante e il valore 1 nel campo 2 viene nascosto.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="a2ed8-128">Si noti che l'allocazione di un record di dimensioni 2 con [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fornisce i campi 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="a2ed8-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="a2ed8-129">Nell'azione personalizzata DLL di esempio seguente viene nascosto il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="a2ed8-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



<span data-ttu-id="a2ed8-130">L'azione personalizzata VBScript seguente nasconde il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="a2ed8-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



