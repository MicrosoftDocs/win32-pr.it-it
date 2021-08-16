---
title: Metodo IConfigAsfWriter GetCurrentProfile
description: Il metodo GetCurrentProfile recupera il profilo definito dall'applicazione.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Metodo GetCurrentProfile windows Media Format
- Metodo GetCurrentProfile in formato Windows Media, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter windows Media Format , metodo GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198382"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Metodo IConfigAsfWriter::GetCurrentProfile

Il **metodo GetCurrentProfile** recupera il profilo definito dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProfile* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore che riceve [**l'interfaccia IWMProfile**](iwmprofile.md) del profilo definito dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, il **puntatore IWMProfile** restituito ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 