---
description: Il metodo di autenticazione dell'APP \_ autentica l'applicazione. Consente a un'applicazione di autenticarsi (usando un protocollo di verifica/firma) quando l'autenticazione viene richiesta da una smart card.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Metodo ISCardAuth:: APP_Auth'
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
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880177"
---
# <a name="iscardauthapp_auth-method"></a>Metodo di autenticazione ISCardAuth:: APP \_

\[Il metodo di **\_ autenticazione dell'app** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo di autenticazione dell' **app \_** autentica l'applicazione. Consente a un'applicazione di autenticarsi (usando un protocollo di verifica/firma) quando l'autenticazione viene richiesta da una [*Smart Card*](../secgloss/s-gly.md).

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

*lAlgoID* \[ in\]
</dt> <dd>

Algoritmo da usare nel processo di autenticazione.

</dd> <dt>

*pParam* \[ in\]
</dt> <dd>

Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.

</dd> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Dati necessari per il calcolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
