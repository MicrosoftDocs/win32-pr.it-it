---
title: Funzione MpThreatQuery (MpClient. h)
description: Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301404"
---
# <a name="mpthreatquery-function"></a>MpThreatQuery (funzione)

Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*ThreatID* \[ in\]
</dt> <dd>

Tipo: **MPTHREAT \_ ID**

Identificatore di minaccia per il quale vengono richieste informazioni.

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Restituisce un puntatore a una struttura di informazioni sulle minacce, [_ *MPTHREAT \_ info* *](mpthreat-info.md). La struttura contiene informazioni quali ID minaccia, nome e gravità.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, facoltativo\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \_ informazioni \* localizzate* _

Restituisce un puntatore a una struttura contenente le informazioni localizzate sulla minaccia. È possibile passare _ *null** se non si è interessati alle informazioni localizzate sulla minaccia. Vedere [**le \_ \_ informazioni localizzate MPTHREAT**](mpthreat-localized-info.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito. Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_informazioni MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**\_informazioni localizzate MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





