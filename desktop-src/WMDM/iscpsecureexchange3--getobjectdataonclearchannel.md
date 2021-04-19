---
title: Metodo GetObjectDataOnClearChannel
description: Il metodo GetObjectDataOnClearChannel trasferisce di nuovo un blocco di dati oggetto su un canale non crittografato a Windows Media Gestione dispositivi.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Metodo GetObjectDataOnClearChannel Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324123"
---
# <a name="getobjectdataonclearchannel-method"></a>Metodo GetObjectDataOnClearChannel

Il metodo **GetObjectDataOnClearChannel** trasferisce di nuovo un blocco di dati oggetto su un canale non crittografato a Windows Media Gestione dispositivi.

Questo metodo è identico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati. Di conseguenza, questo metodo è più efficiente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* 
</dt> <dd>

Puntatore all'oggetto dispositivo.

</dd> <dt>

*pData* 
</dt> <dd>

Puntatore a un buffer per la ricezione dei dati.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Puntatore a un **valore DWORD** che contiene la dimensione di trasferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se il metodo ha esito negativo, viene restituito un codice di errore **HRESULT** .



| Codice restituito                                                                                                | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**Verifica di WMDM \_ E \_ Mac \_ \_ non riuscita**</dt> </dl> | Il codice di autenticazione del messaggio non è valido.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ norights**</dt> </dl>           | Il chiamante non dispone dei diritti necessari per eseguire l'operazione richiesta.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Il metodo non è riuscito. Termina l'interazione con il provider di contenuti.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un parametro è un puntatore **null** o non valido.<br/>                                   |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                     | Si è verificato un errore non specificato.<br/>                                                   |



 

## <a name="remarks"></a>Commenti

Per trasferire dati, Windows Media Gestione dispositivi chiama il metodo [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) per ottenere i dati del contenitore. **GetObjectDataOnClearChannel** viene quindi chiamato per trasferire i blocchi di dati oggetto dal provider di contenuti a Windows Media Gestione dispositivi. Se \_ viene restituito S OK con *pdwSize* impostato su zero, Windows Media Gestione dispositivi non richiederà altri dati.

Questo metodo è identico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati. Di conseguenza, questo metodo è più efficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMSCP. idl</dt> </dl>    |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interfaccia ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





