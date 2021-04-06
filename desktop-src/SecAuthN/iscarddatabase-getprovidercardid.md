---
description: Il metodo GetProviderCardId recupera l'identificatore (GUID) del provider di servizi primario per la smart card specificata.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Metodo ISCardDatabase:: GetProviderCardId (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758825"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>Metodo ISCardDatabase:: GetProviderCardId

\[Il metodo **GetProviderCardId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **GetProviderCardId** recupera l'identificatore (Guid) del [*provider di servizi primario*](../secgloss/p-gly.md) per la [*Smart Card*](../secgloss/s-gly.md)specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrCardName* \[ in\]
</dt> <dd>

Nome della smart card.

</dd> <dt>

*ppguidProviderId* \[ out\]
</dt> <dd>

Puntatore all'identificatore (GUID) del provider di servizi primario in caso di esito positivo; **Null** se l'operazione non è riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                              |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppguidProviderId*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                                  |



 

## <a name="remarks"></a>Commenti

Per elencare le interfacce della smart card, chiamare [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).

Per recuperare tutte le [*Smart Card*](../secgloss/s-gly.md), [*i reader e*](../secgloss/r-gly.md) i [*gruppi di Reader*](../secgloss/r-gly.md) noti, chiamare rispettivamente [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'identificatore del provider di servizi primario per la smart card specificata.


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
