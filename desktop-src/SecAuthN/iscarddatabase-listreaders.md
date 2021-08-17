---
description: Il metodo ListReaders recupera i nomi dei lettori smart card registrati nel database smart card dati.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: Metodo ISCardDatabase::ListReaders (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c7ae9c41a8b1894ec0c233c6090f8ab990e275e95bc20c4768171fe867412838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141134"
---
# <a name="iscarddatabaselistreaders-method"></a>Metodo ISCardDatabase::ListReaders

\[Il **metodo ListReaders** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ListReaders** recupera i nomi dei lettori smart card [*registrati*](../secgloss/r-gly.md) nel database [*smart card .*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*localeId* \[ Pollici\]
</dt> <dd>

ID di localizzazione della lingua.

</dd> <dt>

*ppReaders* \[ Cambio\]
</dt> <dd>

Puntatore a un SAFEARRAY di BSTR che contiene i nomi dei smart card in caso di esito positivo; **NULL se** l'operazione non è riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido in *ppReaders*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                           |



 

## <a name="remarks"></a>Commenti

Per recuperare tutte le [*smart card o*](../secgloss/s-gly.md) i gruppi di lettori noti, chiamare [**rispettivamente ListCards**](iscarddatabase-listcards.md) o [**ListReaderGroups.**](iscarddatabase-listreadergroups.md) [](../secgloss/r-gly.md)

Per recuperare [*rispettivamente il provider di*](../secgloss/p-gly.md) servizi primario o le interfacce di una scheda specifica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces.**](iscarddatabase-listcardinterfaces.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare i nomi smart card lettori registrati nel database smart card dati.


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardDatabase è definito come \_ 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
