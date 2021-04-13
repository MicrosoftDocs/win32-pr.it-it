---
title: Punto di ingresso di VirtualChannelGetInstance
description: Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia IWTSPlugin per tutti i plug-in implementati dalla DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto punto di ingresso di VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400430"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Punto di ingresso di VirtualChannelGetInstance

Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.

> [!Note]
>
> Questa funzione viene implementata dal plug-in e deve essere esportata in base al nome in modo che un'applicazione possa usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico alla funzione.
>
> Il prototipo per questa funzione non è contenuto in un file di intestazione pubblico, quindi è necessario dichiararlo esattamente come illustrato.

 

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

*REFIID* \[ in\]
</dt> <dd>

Specifica il tipo di interfaccia da restituire. Deve essere un **IID \_ IWTSPlugin**.

</dd> <dt>

*pNumObjs* \[ in uscita\]
</dt> <dd>

Indirizzo di una variabile **ULONG** che riceve il numero di interfacce recuperate.

</dd> <dt>

*ppObjArray* \[ out\]
</dt> <dd>

Indirizzo di una matrice di puntatori che riceve i puntatori di interfaccia. Se questo parametro è **null**, l'implementazione deve inserire il numero di plug-in implementati dalla dll nel parametro *pNumObjs* . Ciò consente al chiamante di allocare la matrice di dimensioni appropriate per *ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il punto di ingresso ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

