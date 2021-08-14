---
title: Metodo IConfigAsfWriter GetCurrentProfileGuid
description: Il metodo GetCurrentProfileGuid recupera l'oggetto corrente Windows GUID del profilo di sistema multimediale.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Metodo GetCurrentProfileGuid per Windows Media Format
- Metodo GetCurrentProfileGuid in formato Windows Media, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter windows Media Format, metodo GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433640"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>Metodo IConfigAsfWriter::GetCurrentProfileGuid

Il **metodo GetCurrentProfileGuid** recupera l'oggetto corrente Windows GUID del profilo di sistema multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProfileGuid* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile di tipo **GUID** che identifica il profilo di sistema corrente utilizzato dal filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo non viene usato con i profili personalizzati (inclusi tutti i profili che includono flussi che usano i codec audio e video di Windows) perché tutti questi profili vengono creati dalle applicazioni e non hanno un identificatore GUID. Se non viene caricato alcun profilo di sistema, *pProfileGuid* verrà impostato su **NULL.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 