---
title: Settings. Balance
description: La proprietà Balance specifica o Recupera il saldo stereo corrente.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Impostazioni. bilancia Media Player Windows
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325137"
---
# <a name="settingsbalance"></a>Settings. Balance

La proprietà **Balance** specifica o Recupera il saldo stereo corrente.

## <a name="syntax"></a>Sintassi

Player. Settings. Balance

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Long**). I valori sono compresi tra 100 e 100 e il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Il valore zero indica che l'audio viene riprodotto in un volume uguale sui canali sinistro e destro. Il valore 100 indica che l'audio viene riprodotto solo sul canale sinistro. Il valore 100 indica che l'audio viene riprodotto solo sul canale destro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





