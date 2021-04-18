---
title: Metodo IConfigAsfWriter GetCurrentProfile
description: Il metodo GetCurrentProfile Recupera il profilo definito dall'applicazione.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Metodo GetCurrentProfile Windows Media Format
- Metodo GetCurrentProfile Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299965"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>Metodo IConfigAsfWriter:: GetCurrentProfile

Il metodo **GetCurrentProfile** Recupera il profilo definito dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppProfile* \[ out\]
</dt> <dd>

Indirizzo di un puntatore che riceve l'interfaccia [**IWMProfile**](iwmprofile.md) del profilo definito dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, il puntatore **IWMProfile** restituito ha un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 