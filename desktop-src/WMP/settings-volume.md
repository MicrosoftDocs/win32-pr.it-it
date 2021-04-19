---
title: Settings. volume
description: La proprietà volume specifica o Recupera il volume corrente.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Impostazioni. volume Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327366"
---
# <a name="settingsvolume"></a>Settings. volume

La proprietà **volume** specifica o Recupera il volume corrente.

## <a name="syntax"></a>Sintassi

Player. Settings. volume

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Long**) compreso tra 0 e 100.

## <a name="remarks"></a>Commenti

Zero non specifica alcun volume e 100 specifica il volume completo. Se per questa proprietà non viene specificato alcun valore, per impostazione predefinita viene impostata l'ultima impostazione del volume stabilita per il lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





