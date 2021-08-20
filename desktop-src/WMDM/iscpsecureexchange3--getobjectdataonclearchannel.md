---
title: Metodo GetObjectDataOnClearChannel
description: Il metodo GetObjectDataOnClearChannel trasferisce un blocco di dati oggetto su un canale non crittografato Windows Gestione dispositivi multimediali.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Metodo GetObjectDataOnClearChannel di Gestione dispositivi multimediali
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
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619871"
---
# <a name="getobjectdataonclearchannel-method"></a>Metodo GetObjectDataOnClearChannel

Il **metodo GetObjectDataOnClearChannel** trasferisce un blocco di dati oggetto su un canale non crittografato Windows Gestione dispositivi multimediali.

Questo metodo è identico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati. Di conseguenza, questo metodo è più efficiente.

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

Puntatore a un buffer per ricevere i dati.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Puntatore a un **valore DWORD** contenente le dimensioni del trasferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se il metodo ha esito negativo, restituisce un **codice di errore HRESULT.**



| Codice restituito                                                                                                | Descrizione                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLLO WMDM \_ E \_ MAC NON \_ \_ RIUSCITO**</dt> </dl> | Il codice di autenticazione del messaggio non è valido.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ NORIGHTS**</dt> </dl>           | Il chiamante non dispone dei diritti necessari per eseguire l'operazione richiesta.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Il metodo non è riuscito. Termina l'interazione con il provider di contenuti.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un parametro è un puntatore **null o non** valido.<br/>                                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Si è verificato un errore non specificato.<br/>                                                   |



 

## <a name="remarks"></a>Commenti

Per trasferire i dati, Windows Gestione dispositivi multimediali chiama il [metodo TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) per ottenere i dati del contenitore. **GetObjectDataOnClearChannel viene** quindi chiamato per trasferire blocchi di dati oggetto dal provider di contenuti Windows Gestione dispositivi multimediali. Se viene restituito S \_ OK con *pdwSize* impostato su zero, Windows Gestione dispositivi multimediali non richiederà altri dati.

Questo metodo è identico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati. Di conseguenza, questo metodo è più efficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMSCP.idl</dt> </dl>    |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interfaccia ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





