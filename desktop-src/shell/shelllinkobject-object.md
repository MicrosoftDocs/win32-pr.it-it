---
description: Gestisce i collegamenti della shell. Questo oggetto rende disponibile gran parte delle funzionalità dell'interfaccia IShellLink alle applicazioni di scripting.
title: Oggetto ShellLinkObject (Shldisp.h)
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
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842632"
---
# <a name="shelllinkobject-object"></a>Oggetto ShellLinkObject

Gestisce i collegamenti della shell. Questo oggetto rende disponibile gran parte delle funzionalità [**dell'interfaccia IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) alle applicazioni di scripting.

## <a name="members"></a>Membri

**L'oggetto ShellLinkObject** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto ShellLinkObject** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Ottiene il percorso dell'icona assegnata al collegamento.<br/>                                 |
| [**Risolvi**](shelllinkobject-resolve.md)                 | Cerca la destinazione di un collegamento shell, anche se la destinazione è stata spostata o rinominata.<br/> |
| [**Salva**](shelllinkobject-save.md)                       | Salva tutte le modifiche apportate al collegamento.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Imposta la posizione dell'icona assegnata al collegamento.<br/>                                 |



 

### <a name="properties"></a>Proprietà

**L'oggetto ShellLinkObject** ha queste proprietà.



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
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamenti alla shell](./links.md)
</dt> </dl>

 

 
