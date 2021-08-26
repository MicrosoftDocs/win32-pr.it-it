---
title: Punto di ingresso VirtualChannelGetInstance
description: Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia IWTSPlugin per tutti i plug-in implementati dalla DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Punto di ingresso VirtualChannelGetInstance Servizi Desktop remoto
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f96eac56f737d6f945c3d59d5cdf844e9cc65058a0460f620e6051830806ab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868621"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Punto di ingresso VirtualChannelGetInstance

Chiamato per fare in modo che il plug-in crei un'istanza [**dell'interfaccia IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla DLL.

> [!Note]
>
> Questa funzione viene implementata dal plug-in e deve essere esportata in base al nome in modo che un'applicazione possa usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico alla funzione.
>
> Il prototipo per questa funzione non è contenuto in alcun file di intestazione pubblico, pertanto è necessario dichiararlo esattamente come illustrato.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*refiid* \[ Pollici\]
</dt> <dd>

Specifica il tipo di interfaccia da restituire. Deve essere **IID \_ IWTSPlugin.**

</dd> <dt>

*pNumObjs* \[ in, out\]
</dt> <dd>

Indirizzo di una **variabile ULONG** che riceve il numero di interfacce recuperate.

</dd> <dt>

*ppObjArray* \[ Cambio\]
</dt> <dd>

Indirizzo di una matrice di puntatori che riceve i puntatori a interfaccia. Se questo parametro è **NULL,** l'implementazione deve inserire il numero di plug-in implementati dalla DLL nel *parametro pNumObjs.* Ciò consente al chiamante di allocare la matrice di dimensioni appropriata *per ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo punto di ingresso ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

