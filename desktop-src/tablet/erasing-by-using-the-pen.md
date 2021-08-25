---
description: Se si sceglie di implementare la cancellazione nell'applicazione diversa dall'uso dell'oggetto InkOverlay, è possibile usare uno dei due metodi seguenti.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Cancellazione tramite l'oggetto Pen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96d7d281f4e94a4a53f7e99e83c38192ceb7d31fbf9ee643653a20b4836a7cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936571"
---
# <a name="erasing-by-using-the-pen"></a>Cancellazione tramite l'oggetto Pen

Se si sceglie di implementare la cancellazione nell'applicazione diversa dall'uso dell'oggetto [**InkOverlay,**](inkoverlay-class.md) è possibile usare uno dei due metodi seguenti.

## <a name="using-the-tip-of-the-pen"></a>Uso della punta della penna

La punta della penna del tablet viene in genere usata per la scrittura manuale e il disegno. Tuttavia, la mancia può essere usata anche per cancellare l'input penna. A tale scopo, l'applicazione deve avere una modalità di cancellazione che gli utenti possono usare. In questa modalità, usare l'hit testing per determinare l'input penna su cui si sposta il cursore. È possibile impostare la modalità di cancellazione in modo da eliminare solo l'input penna passato dal cursore o tratti interi che intersecano il percorso del cursore, a seconda della progettazione o delle considerazioni funzionali.

Per un esempio di come usare una modalità di cancellazione per cancellare l'input penna, vedere l'esempio [di cancellazione dell'input penna](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Uso della parte superiore dell'oggetto Pen

Per implementare la cancellazione con la parte superiore della penna del tablet, l'applicazione deve cercare una modifica nel cursore. Per cercare il cursore invertito, restare in ascolto [**dell'evento CursorInRange**](inkoverlay-cursorinrange.md) per determinare quando il cursore si trova nel contesto dell'applicazione. Quando il cursore è compreso nell'intervallo, cercare la [**proprietà Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) nell'oggetto [**Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Se la **proprietà Inverted** è **true,** eseguire l'hit testing per determinare l'input penna su cui si sposta il cursore. Cancellare l'input penna o i tratti che intersecano il percorso del cursore, a seconda della progettazione o delle considerazioni funzionali.

Per un esempio di come usare la parte superiore della penna per cancellare l'input penna, vedere l'esempio [di cancellazione dell'input penna](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Determinare se la cancellazione con la parte superiore della penna è abilitata

Gli utenti possono usare la parte superiore della penna per cancellare l'input penna nelle applicazioni progettate per Tablet PC, se il proprio hardware specifico lo consente. Questa funzionalità è accessibile da una casella di controllo nella casella di gruppo Pulsanti penna della scheda Opzioni penna della finestra di dialogo Impostazioni pannello di controllo. Per rilevare se l'utente ha abilitato la cancellazione per la parte superiore della penna, controllare la sottochiave del Registro di sistema seguente:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

La `EraseEnable` voce di questa sottochiave è di tipo REG **\_ DWORD**. Il valore di questa voce è 1 per enabled o 0 per disabled. Altri valori sono riservati per utilizzi futuri.

Se l'applicazione consente l'uso della parte superiore della penna per la cancellazione, è necessario controllare e memorizzare nella cache il valore della voce EraseEnable quando:

-   Viene avviata l'applicazione.
-   Ogni volta che l'applicazione riceve lo stato attivo dopo aver perso lo stato attivo.

Usare questo valore memorizzato nella cache per modificare il comportamento dell'applicazione in modo appropriato.

Nell'esempio C \# seguente viene definito un metodo che controlla il valore della voce della `GetEraseEnabled` `EraseEnable` `SysEventParameters` sottochiave. Il metodo restituisce TRUE se il valore della voce è 1; restituisce FALSE se il valore della voce è 0 oppure genera un'eccezione `GetEraseEnabled` [InvalidOperationException](/dotnet/api/system.invalidoperationexception)  se il valore della voce è diverso da 1 o 0.  Il `GetEraseEnabled` metodo restituisce il valore previsto **TRUE** se la sottochiave o la voce non è presente.


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



 

 
