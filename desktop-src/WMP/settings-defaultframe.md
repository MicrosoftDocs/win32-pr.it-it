---
title: Settings. defaultFrame
description: La proprietà defaultFrame specifica o Recupera il nome del frame usato per visualizzare un URL ricevuto in un evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Impostazioni. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327982"
---
# <a name="settingsdefaultframe"></a>Settings. defaultFrame

La proprietà **DefaultFrame** specifica o Recupera il nome del frame usato per visualizzare un URL ricevuto in un evento **ScriptCommand** .

## <a name="syntax"></a>Sintassi

Player. Settings. defaultFrame

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura che corrisponde al valore dell'attributo **Name** dell'elemento frame di destinazione.

## <a name="remarks"></a>Commenti

Se un frame di destinazione viene specificato nell'evento **ScriptCommand** stesso, questa proprietà viene ignorata.

Questa proprietà viene ignorata quando si usa l'applet Java del navigatore Netscape. In Navigator ogni comando script URL ricevuto Visualizza l'URL in una nuova finestra del browser, indipendentemente dal valore delle *Impostazioni*. **DefaultFrame**.

**Windows Media Player 10 Mobile**: questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Uso di Windows Media Player con Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





