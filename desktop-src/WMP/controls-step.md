---
title: Metodo Controls. Step
description: Il metodo Step fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo o nel frame precedente.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Metodo Step Media Player Windows
- Metodo Step Media Player Windows, classe Controls
- Classe Controls Media Player Windows, Metodo Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327390"
---
# <a name="controlsstep-method"></a>Metodo Controls. Step

Il metodo **Step** fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo o nel frame precedente.

## <a name="syntax"></a>Sintassi


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*frameCount* \[ in\]
</dt> <dd>

**Numero** (**Long**) che indica il numero di frame da scorrere prima del blocco. Attualmente deve essere impostato su 1 o-1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo supporta attualmente solo i parametri 1 o-1, pertanto è possibile eseguire un solo passaggio di un frame alla volta.

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> </dl>

 

 





