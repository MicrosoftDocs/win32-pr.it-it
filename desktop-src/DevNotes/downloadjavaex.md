---
description: Scarica la firma del file CAB, verifica le autorizzazioni associate ai pacchetti e le esegue in base all'autenticazione.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328567"
---
# <a name="downloadjavaex-function"></a>DownloadJavaEX (funzione)

Scarica la firma del file CAB, verifica le autorizzazioni associate ai pacchetti e le esegue in base all'autenticazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Riservato* \[ in\]
</dt> <dd>

Questo parametro è riservato.

</dd> <dt>

*pProviderData* \[ in\]
</dt> <dd>

Struttura [**di \_ \_ dati del provider di crittografia**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) che contiene i dati del certificato, ad esempio le autorizzazioni per file e zone.

</dd> <dt>

*pJava* \[ in\]
</dt> <dd>

Struttura [**del \_ \_ provider di criteri Java**](/previous-versions//bb432350(v=vs.85)) che contiene i dati relativi al provider di criteri.

</dd> <dt>

*pFunctions* \[ in\]
</dt> <dd>

Struttura [**di \_ \_ funzioni del provider di crittografia**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) contenente un elenco di metodi per verificare gli oggetti certificato, le firme e i criteri finali.

</dd> <dt>

*fCertificate* \[ in\]
</dt> <dd>

Se è presente un certificato, questo parametro è **true**. In caso contrario, è **false**.

</dd> <dt>

*pTrust* \[ in\]
</dt> <dd>

Struttura [**di \_ attendibilità Java**](/windows/desktop/api/Capi/ns-capi-java_trust) che contiene informazioni sull'attendibilità, ad esempio autorizzazione codificata, firma del codificatore e codice dei criteri di restituzione autentico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **\_ OK**. In caso contrario, il valore restituito è un codice di errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
