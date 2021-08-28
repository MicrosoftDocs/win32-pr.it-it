---
description: Il metodo GetProviderCardId recupera l'identificatore (GUID) del provider di servizi primario per il smart card.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: Metodo ISCardDatabase::GetProviderCardId (Scardmgr.h)
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
ms.openlocfilehash: 814eec89f8ff92d81dd911101d79e516500f0baeb363dd4148bd466de849bc24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577281"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>Metodo ISCardDatabase::GetProviderCardId

\[Il **metodo GetProviderCardId** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetProviderCardId** recupera l'identificatore (GUID) del provider di servizi [*primario*](../secgloss/p-gly.md) per l'smart card . [](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrCardName* \[ Pollici\]
</dt> <dd>

Nome del smart card.

</dd> <dt>

*ppguidProviderId* \[ Cambio\]
</dt> <dd>

Puntatore all'identificatore (GUID) del provider di servizi primario in caso di esito positivo; **NULL se** l'operazione non è riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                              |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *ppguidProviderId*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                  |



 

## <a name="remarks"></a>Commenti

Per elencare le interfacce del smart card, chiamare [**ListCardInterfaces.**](iscarddatabase-listcardinterfaces.md)

Per recuperare tutte le [](../secgloss/r-gly.md) smart [](../secgloss/r-gly.md) [*card note,*](../secgloss/s-gly.md)i lettori e i gruppi di lettori chiamano [**rispettivamente ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups.**](iscarddatabase-listreadergroups.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase.**](iscarddatabase.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'identificatore del provider di servizi primario per l'smart card.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
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

[**ListReader**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
