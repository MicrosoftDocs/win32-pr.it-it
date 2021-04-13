---
title: Metodo IConfigAsfWriter GetCurrentProfileGuid
description: Il metodo GetCurrentProfileGuid Recupera il GUID del profilo di sistema Windows Media corrente.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Metodo GetCurrentProfileGuid Windows Media Format
- Metodo GetCurrentProfileGuid Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338798"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Metodo IConfigAsfWriter:: GetCurrentProfileGuid

Il metodo **GetCurrentProfileGuid** Recupera il GUID del profilo di sistema Windows Media corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProfileGuid* \[ out\]
</dt> <dd>

Puntatore a una variabile di tipo **GUID** che identifica il profilo di sistema corrente utilizzato dal filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo non viene usato con i profili personalizzati (inclusi tutti i profili che includono flussi che usano i codec Windows Media Audio e video) perché tutti questi profili vengono creati dalle applicazioni e non hanno un identificatore GUID. Se non viene caricato alcun profilo di sistema, *pProfileGuid* verrà impostato su **null**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 