---
description: Se si sceglie di implementare la cancellazione nell'applicazione diversa da tramite l'oggetto InkOverlay, è possibile eseguire questa operazione utilizzando uno dei due metodi seguenti.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Cancellazione tramite penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401659"
---
# <a name="erasing-by-using-the-pen"></a>Cancellazione tramite penna

Se si sceglie di implementare la cancellazione nell'applicazione diversa da tramite l'oggetto [**InkOverlay**](inkoverlay-class.md) , è possibile eseguire questa operazione utilizzando uno dei due metodi seguenti.

## <a name="using-the-tip-of-the-pen"></a>Uso del suggerimento della penna

Il suggerimento della penna del Tablet viene in genere usato per la grafia e il disegno; Tuttavia, il suggerimento può essere usato anche per cancellare l'input penna. A tale scopo, è necessario che l'applicazione disponga di una modalità di cancellazione che gli utenti possono utilizzare. In questa modalità, utilizzare hit testing per determinare l'input penna su cui si sta muovendo il cursore. È possibile impostare la modalità di cancellazione per eliminare solo l'input penna passato dal cursore o interi tratti che intersecano il percorso del cursore, a seconda delle considerazioni sulla progettazione o sulle funzionalità.

Per un esempio di come usare una modalità di cancellazione per cancellare l'input penna, vedere l' [esempio di cancellazione di input penna](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Uso della parte superiore della penna

Per implementare la cancellazione con la parte superiore della penna del tablet, l'applicazione deve cercare una modifica nel cursore. Per cercare il cursore invertito, attendere l'evento [**CursorInRange**](inkoverlay-cursorinrange.md) per determinare quando il cursore si trova all'interno del contesto dell'applicazione. Quando il cursore si trova nell'intervallo, cercare la proprietà [**invertita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sull'oggetto [**cursore**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Se la proprietà **invertita** è **true**, eseguire l'hit testing per determinare l'input penna su cui si sta muovendo il cursore. Cancellare l'input penna o i tratti che intersecano il percorso del cursore, a seconda delle considerazioni sulla progettazione o sulle funzionalità.

Per un esempio di come usare la parte superiore della penna per cancellare l'input penna, vedere l' [esempio di cancellazione di input penna](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Determinazione della cancellazione con la parte superiore della penna abilitata

Gli utenti possono utilizzare la parte superiore della penna per cancellare l'input penna in applicazioni progettate per Tablet PC, se il relativo hardware specifico lo supporta. Questa funzionalità è accessibile da una casella di controllo nella casella di gruppo pulsanti penna nella scheda Opzioni penna della finestra di dialogo Pannello di controllo Impostazioni Tablet e penna. Per rilevare se l'utente ha abilitato la cancellazione per la parte superiore della penna, controllare la seguente sottochiave del registro di sistema:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

La `EraseEnable` voce della sottochiave è di tipo **reg \_ DWORD**. Il valore di questa voce è 1 per Enabled oppure 0 per Disabled. Altri valori sono riservati per utilizzi futuri.

Se l'applicazione consente di usare la parte superiore della penna per la cancellazione, è consigliabile controllare e memorizzare nella cache il valore della voce EraseEnable quando:

-   Viene avviata l'applicazione.
-   Ogni volta che l'applicazione riceve lo stato attivo dopo aver perso lo stato attivo.

Utilizzare questo valore memorizzato nella cache per modificare il comportamento dell'applicazione in modo appropriato.

Nell'esempio C seguente \# viene definito un `GetEraseEnabled` metodo che controlla il valore della `EraseEnable` voce della `SysEventParameters` sottochiave. Il `GetEraseEnabled` metodo restituisce **true** se il valore della voce è 1. restituisce **false** se il valore della voce è 0 oppure genera un'eccezione [InvalidOperationException](/dotnet/api/system.invalidoperationexception) se il valore della voce è diverso da 1 o 0. Il `GetEraseEnabled` metodo restituisce il valore previsto **true** se la sottochiave o la voce non è presente.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
