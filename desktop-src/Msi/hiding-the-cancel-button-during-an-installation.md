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
# <a name="hiding-the-cancel-button-during-an-installation"></a>Nascondere il pulsante Annulla durante un'installazione

È possibile nascondere il pulsante **Annulla** usato per annullare un'installazione usando un'opzione della riga di comando, l'API Windows Installer o un'azione personalizzata. Il pulsante **Annulla** può essere nascosto per una parte o per tutte le installazioni a seconda del metodo usato.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Nascondere il pulsante Annulla dalla riga di comando

Il pulsante **Annulla** può essere nascosto durante l'installazione tramite l'opzione della riga di comando (!). Questa operazione può essere eseguita solo per un'installazione di base a livello di interfaccia utente (/QB). Il pulsante **Annulla** è nascosto per l'intera installazione. Per altre informazioni, vedere [Opzioni della riga di comando](command-line-options.md) e [livelli dell'interfaccia utente](user-interface-levels.md). La riga di comando seguente nasconde il pulsante **Annulla** e installa Example.msi.

**msiexec/I example.msi/QB!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Nascondere il pulsante Annulla da un'applicazione o da uno script

È possibile scrivere un'applicazione o uno script per nascondere il pulsante **Annulla** . Questa operazione può essere eseguita solo per un'installazione a livello di interfaccia utente di base, in modo che il pulsante **Annulla** sia nascosto per l'intera installazione.

Per nascondere il pulsante Annulla da un'applicazione, impostare INSTALLUILEVEL \_ HIDECANCEL quando si chiama [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Nell'esempio seguente viene nascosto il pulsante **Annulla** e viene installato Example.msi.


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



Per nascondere il pulsante **Annulla** dallo script, aggiungere msiUILevelHideCancel alla proprietà [**UILevel**](installer-uilevel.md) dell' [**oggetto Installer**](installer-object.md). Nell'esempio VBScript seguente viene nascosto il pulsante **Annulla** e viene installato Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Nascondere il pulsante Annulla per parti di un'installazione mediante un'azione personalizzata

L'installazione può nascondere e scoprire il pulsante **Annulla** durante le parti di un'installazione inviando un \_ messaggio INSTALLMESSAGE COMMONDATA utilizzando un'azione o script personalizzati della dll. Per altre informazioni, vedere [librerie a collegamento dinamico](dynamic-link-libraries.md), [script](scripts.md), [azioni personalizzate](custom-actions.md)e [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Una chiamata a un'azione personalizzata deve fornire un record. Il campo 1 di questo record deve contenere il valore 2 (due) per specificare il pulsante **Annulla** . Il campo 2 deve contenere il valore 0 o 1. Il valore 0 nel campo 2 nasconde il pulsante e il valore 1 nel campo 2 viene nascosto. Si noti che l'allocazione di un record di dimensioni 2 con [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) fornisce i campi 0, 1 e 2.

Nell'azione personalizzata DLL di esempio seguente viene nascosto il pulsante **Annulla** .


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



L'azione personalizzata VBScript seguente nasconde il pulsante **Annulla** .


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



 

 



