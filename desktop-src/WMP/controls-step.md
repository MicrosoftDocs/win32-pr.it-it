---
title: Metodo Controls.step
description: Il metodo step fa sì che l'elemento multimediale video corrente blocchi la riproduzione nel fotogramma successivo o nel fotogramma precedente.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Metodo step Windows Media Player
- Metodo step Windows Media Player , classe Controls
- Classe Controls Windows Media Player , metodo step
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
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839826"
---
# <a name="controlsstep-method"></a>Metodo Controls.step

Il **metodo step** fa sì che l'elemento multimediale video corrente blocchi la riproduzione nel fotogramma successivo o nel fotogramma precedente.

## <a name="syntax"></a>Sintassi


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*frameCount* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che indica il numero di fotogrammi da eseguire prima del blocco. Attualmente deve essere impostato su 1 o -1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo attualmente supporta solo i parametri 1 o -1, quindi è possibile eseguire un solo fotogramma alla volta.

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

 

 





