---
description: Scarica la .cab del file, verifica le autorizzazioni associate ai pacchetti ed esegue le autorizzazioni in base all'autenticazione.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Funzione DownloadJavaEX
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
ms.openlocfilehash: 628fdb1b8b0ec9979d844c8f48fb02fbf8f6a642a96c925f427c868160dd6b27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795261"
---
# <a name="downloadjavaex-function"></a>Funzione DownloadJavaEX

Scarica la .cab del file, verifica le autorizzazioni associate ai pacchetti ed esegue le autorizzazioni in base all'autenticazione.

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

*Riservato* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato.

</dd> <dt>

*pProviderData* \[ Pollici\]
</dt> <dd>

Struttura [**CRYPT \_ PROVIDER \_ DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) che contiene i dati del certificato, ad esempio le autorizzazioni per file e zone.

</dd> <dt>

*pJava* \[ Pollici\]
</dt> <dd>

Struttura [**DEL PROVIDER DI \_ \_ CRITERI JAVA**](/previous-versions//bb432350(v=vs.85)) che contiene i dati correlati al provider di criteri.

</dd> <dt>

*pFunctions* \[ Pollici\]
</dt> <dd>

Struttura [**CRYPT \_ PROVIDER \_ FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) che contiene un elenco di metodi per verificare gli oggetti certificato, le firme e i criteri finali.

</dd> <dt>

*fCertificate* \[ Pollici\]
</dt> <dd>

Se è presente un certificato, questo parametro è **TRUE.** In caso contrario, è **FALSE.**

</dd> <dt>

*pTrust* \[ Pollici\]
</dt> <dd>

Struttura [**TRUST JAVA \_ che**](/windows/desktop/api/Capi/ns-capi-java_trust) contiene informazioni sull'attendibilità, ad esempio l'autorizzazione codificata, la firma del codificatore e il codice dei criteri restituiti autenticati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**. In caso contrario, il valore restituito è un codice di errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
