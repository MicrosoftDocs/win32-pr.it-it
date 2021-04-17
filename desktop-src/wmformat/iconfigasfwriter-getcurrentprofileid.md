---
title: Metodo IConfigAsfWriter GetCurrentProfileId
description: Il metodo GetCurrentProfileId recupera l'ID del profilo corrente. (Solo per i profili Windows Media Format 4,0).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Metodo GetCurrentProfileId Windows Media Format
- Metodo GetCurrentProfileId Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299964"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>Metodo IConfigAsfWriter:: GetCurrentProfileId

Il metodo **GetCurrentProfileId** recupera l'ID del profilo corrente. (Solo per i profili Windows Media Format 4,0).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwProfileId* \[ out\]
</dt> <dd>

Puntatore a una variabile di tipo **DWORD** che riceve l'ID del profilo corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo è ora obsoleto perché presuppone la versione 4,0 di profili SDK di formato Windows Media. Usare invece [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) o [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) per identificare correttamente un profilo per la versione 7,0 e successive.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 