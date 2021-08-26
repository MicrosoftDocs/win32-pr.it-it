---
description: Il metodo \_ app Auth autentica l'applicazione. Consente a un'applicazione di autenticarsi (usando un protocollo di verifica/firma) quando l'autenticazione viene richiesta da un smart card.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: Metodo ISCardAuth::APP_Auth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: db6d2b673caf15d5d15e63894a6c5a589fd2d18ea031a3201a562f255ee6cf2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015551"
---
# <a name="iscardauthapp_auth-method"></a>Metodo di autenticazione ISCardAuth::APP \_

\[Il **metodo \_ app Auth** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo \_ app Auth** autentica l'applicazione. Consente a un'applicazione di autenticarsi (usando un protocollo di [*verifica/firma)*](../secgloss/s-gly.md)quando l'autenticazione viene richiesta da un smart card .

## <a name="syntax"></a>Sintassi


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lAlgoID* \[ Pollici\]
</dt> <dd>

Algoritmo da usare nel processo di autenticazione.

</dd> <dt>

*pParam* \[ Pollici\]
</dt> <dd>

[**IByteBuffer contenente**](ibytebuffer.md) i parametri specifici del fornitore del processo di autenticazione.

</dd> <dt>

*pBuffer* \[ Pollici\]
</dt> <dd>

Dati necessari per il calcolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
