---
description: La proprietà UILevel dell'oggetto Installer è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da usare per l'apertura e l'elaborazione dei pacchetti successivi all'interno dello spazio del processo corrente.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Proprietà Installer.UILevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3004675ee8e07c3503ec4442832c00975364066fa4a0c770b0b081fc7b64c3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043571"
---
# <a name="installeruilevel-property"></a>Proprietà Installer.UILevel

La **proprietà UILevel** dell'oggetto [**Installer**](installer-object.md) è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da usare per l'apertura e l'elaborazione dei pacchetti successivi all'interno dello spazio del processo corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti



| Livello dell'interfaccia utente   | Valore | Descrizione                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | Non modifica il livello dell'interfaccia utente.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Usa il livello predefinito dell'interfaccia utente.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Installazione invisibile all'utente.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Semplice gestione dello stato di avanzamento e degli errori.                                                                                                                                                                |
| msiUILevelReduced      | 4     | L'interfaccia utente e le finestre di dialogo della procedura guidata sono stati eliminati.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interfaccia utente personalizzata con procedure guidate, stato di avanzamento ed errori.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Se combinato con il valore msiUILevelBasic, il programma di  installazione visualizza le finestre di dialogo di stato, ma non visualizza un pulsante Annulla nella finestra di dialogo per impedire agli utenti di annullare l'installazione. |
| msiUILevelProgressOnly | 64    | Se combinato con il valore msiUILevelBasic, il programma di installazione visualizza le finestre di dialogo di stato, ma non visualizza finestre di dialogo modali o finestre di dialogo di errore.                                        |
| MsiUILevelEndDialog    | 128   | Se combinato con qualsiasi valore precedente, il programma di installazione visualizza una finestra di dialogo modale al termine di un'installazione corretta o se si è verificato un errore. Se l'utente annulla, non viene visualizzata alcuna finestra di dialogo. |



 

Vedere anche [Determinare il livello dell'interfaccia utente da un'azione personalizzata.](determining-ui-level-from-a-custom-action.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




