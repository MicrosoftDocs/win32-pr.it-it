---
description: Crea un gestore del flusso di byte per l'origine multimediale MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Funzione MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: c2d2d07905932e589e8873722bd0889cec6dc321c28dbc2d1c8704f880df4991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690973"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>Funzione MFCreateMP3ByteStreamPlugin

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono invece usare il [sistema di risoluzione dei problemi di](source-resolver.md) origine per creare l'origine multimediale MP3.\]

Crea un gestore del flusso di byte per l'origine multimediale MP3.

## <a name="syntax"></a>Sintassi


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ Pollici\]
</dt> <dd>

Identificatore di interfaccia (IID) dell'interfaccia richiesta. Impostare questo parametro su **IID \_ IMFByteStreamHandler** per ricevere un puntatore [**all'interfaccia IMFByteStreamHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)

</dd> <dt>

*ppvHandler* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia . Il chiamante deve rilasciare l'interfaccia .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente mf.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |
| Fine del supporto client<br/>    | Windows Vista<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation funzioni](media-foundation-functions.md)
</dt> <dt>

[Gestori di schemi e Byte-Stream di schema](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 
