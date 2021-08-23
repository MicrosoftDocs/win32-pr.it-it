---
title: Impostazioni.defaultFrame
description: La proprietà defaultFrame specifica o recupera il nome del frame usato per visualizzare un URL ricevuto in un evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Impostazioni.defaultFrame Windows Media Player
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
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571811"
---
# <a name="settingsdefaultframe"></a>Impostazioni.defaultFrame

La **proprietà defaultFrame** specifica o recupera il nome del frame usato per visualizzare un URL ricevuto in un **evento ScriptCommand.**

## <a name="syntax"></a>Sintassi

player.settings.defaultFrame

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una  stringa di lettura/scrittura corrispondente al valore dell'attributo **name** dell'elemento FRAME di destinazione.

## <a name="remarks"></a>Commenti

Se nell'evento **ScriptCommand** viene specificato un frame di destinazione, questa proprietà viene ignorata.

Questa proprietà viene ignorata quando si usa Netscape Navigator applet Java. In Strumento di navigazione ogni comando di script URL ricevuto visualizza l'URL in una nuova finestra del browser, indipendentemente dal valore *di Impostazioni*. **defaultFrame**.

**Windows Media Player 10 Mobile:** questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Uso di Windows Media Player con Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





