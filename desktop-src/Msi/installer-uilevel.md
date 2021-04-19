---
description: La proprietà UILevel dell'oggetto Installer è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da utilizzare per l'apertura e l'elaborazione di pacchetti successivi nello spazio di processo corrente.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Proprietà Installer. UILevel
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
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333165"
---
# <a name="installeruilevel-property"></a>Proprietà Installer. UILevel

La proprietà **UILevel** dell'oggetto [**Installer**](installer-object.md) è una proprietà di lettura/scrittura che indica il tipo di interfaccia utente da utilizzare per l'apertura e l'elaborazione di pacchetti successivi nello spazio di processo corrente.

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
| msiUILevelDefault      | 1     | Usa il livello di interfaccia utente predefinito.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Installazione invisibile all'utente.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Semplice gestione degli errori e dello stato di avanzamento.                                                                                                                                                                |
| msiUILevelReduced      | 4     | Finestre di dialogo dell'interfaccia utente e della procedura guidata Create ed eliminati.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interfaccia utente creata con procedure guidate, stato ed errori.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Se combinato con il valore msiUILevelBasic, il programma di installazione Mostra le finestre di dialogo di stato ma non visualizza un pulsante **Annulla** nella finestra di dialogo per impedire agli utenti di annullare l'installazione. |
| msiUILevelProgressOnly | 64    | Se combinato con il valore msiUILevelBasic, nel programma di installazione vengono visualizzate le finestre di dialogo di stato ma non vengono visualizzate finestre di dialogo modali o finestre di dialogo di errore.                                        |
| msiUILevelEndDialog    | 128   | Se combinato con qualsiasi valore precedente, il programma di installazione visualizza una finestra di dialogo modale alla fine di una corretta installazione o se si è verificato un errore. Se l'utente Annulla, non verrà visualizzata alcuna finestra di dialogo. |



 

Vedere anche [determinazione del livello dell'interfaccia utente da un'azione personalizzata](determining-ui-level-from-a-custom-action.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




