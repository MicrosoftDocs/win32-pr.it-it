---
title: Impostazioni.volume
description: La proprietà volume specifica o recupera il volume corrente.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Impostazioni.volume Windows Media Player
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
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002211"
---
# <a name="settingsvolume"></a>Impostazioni.volume

La **proprietà volume** specifica o recupera il volume corrente.

## <a name="syntax"></a>Sintassi

player.settings.volume

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**long**) compreso tra 0 e 100.

## <a name="remarks"></a>Commenti

Zero non specifica alcun volume e 100 specifica il volume completo. Se non viene specificato alcun valore per questa proprietà, per impostazione predefinita viene impostata l'ultima impostazione del volume stabilita per il lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





