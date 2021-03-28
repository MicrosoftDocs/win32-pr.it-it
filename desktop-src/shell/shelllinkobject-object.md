---
description: Gestisce i collegamenti della shell. Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia IShellLink disponibili per le applicazioni di scripting.
title: Oggetto ShellLinkObject (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980730"
---
# <a name="shelllinkobject-object"></a>Oggetto ShellLinkObject

Gestisce i collegamenti della shell. Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) disponibili per le applicazioni di scripting.

## <a name="members"></a>Membri

L'oggetto **ShellLinkObject** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **ShellLinkObject** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Ottiene la posizione dell'icona assegnata al collegamento.<br/>                                 |
| [**Risolvi**](shelllinkobject-resolve.md)                 | Cerca la destinazione di un collegamento della shell, anche se la destinazione è stata spostata o rinominata.<br/> |
| [**Salva**](shelllinkobject-save.md)                       | Salva tutte le modifiche apportate al collegamento.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Imposta la posizione dell'icona assegnata al collegamento.<br/>                                 |



 

### <a name="properties"></a>Proprietà

L'oggetto **ShellLinkObject** dispone di queste proprietà.



| Proprietà                                                                | Tipo di accesso           | Descrizione                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argomenti**](shelllinkobject-arguments.md)<br/>               | Lettura/Scrittura<br/> | Contiene gli argomenti di un collegamento.<br/>                                                                   |
| [**Descrizione**](shelllinkobject-description.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta la descrizione del collegamento.<br/>                                                      |
| [**Tasto di scelta rapida**](shelllinkobject-hotkey.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta il tasto di scelta rapida per il collegamento.<br/>                                               |
| [**Percorso**](shelllinkobject-path.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il percorso dell'oggetto collegamento.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta lo stato di visualizzazione iniziale (ridimensionato, ridotto a icona o ingrandito) del comando del collegamento.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la directory di lavoro specificata nel collegamento.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamenti Shell](./links.md)
</dt> </dl>

 

 
