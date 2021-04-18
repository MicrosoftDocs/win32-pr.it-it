---
description: Crea un gestore del flusso di byte per l'origine dei supporti MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin (funzione)
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
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308413"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>MFCreateMP3ByteStreamPlugin (funzione)

\[Questa API non è supportata e può essere modificata o non disponibile in futuro. Al contrario, le applicazioni devono usare il [resolver di origine](source-resolver.md) per creare l'origine multimediale MP3.\]

Crea un gestore del flusso di byte per l'origine dei supporti MP3.

## <a name="syntax"></a>Sintassi


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Identificatore di interfaccia (IID) dell'interfaccia richiesta. Impostare questo parametro su **IID \_ IMFByteStreamHandler** per ricevere un puntatore all'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .

</dd> <dt>

*ppvHandler* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia. Il chiamante deve rilasciare l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a mf.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |
| Fine del supporto client<br/>    | Windows Vista<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni Media Foundation](media-foundation-functions.md)
</dt> <dt>

[Gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 
