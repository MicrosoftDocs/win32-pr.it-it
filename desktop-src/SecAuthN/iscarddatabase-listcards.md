---
description: Il metodo ListCards recupera tutti i nomi smart card che corrispondono ai GUID (Interface Identifier) specificati, alla stringa ATR specificata o a entrambi.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: Metodo ISCardDatabase::ListCards (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c34d5d1449b2ef8f34fa87d3a70ecf37787d423a0d5df71ecd15e5f722d112ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014531"
---
# <a name="iscarddatabaselistcards-method"></a>Metodo ISCardDatabase::ListCards

\[Il **metodo ListCards** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ListCards** recupera tutti i nomi smart card che corrispondono ai GUID (Interface Identifier) specificati, alla stringa [*ATR*](../secgloss/a-gly.md)specificata o a entrambi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAtr* \[ Pollici\]
</dt> <dd>

Puntatore a una [*smart card*](../secgloss/s-gly.md) ATR. La stringa ATR deve essere in pacchetto in [**un oggetto IByteBuffer**](ibytebuffer.md).

</dd> <dt>

*pInterfaceGuids* \[ Pollici\]
</dt> <dd>

Puntatore a un SAFEARRAY di identificatori di interfaccia COM (GUID) in formato BSTR.

</dd> <dt>

*localeId* \[ Pollici\]
</dt> <dd>

Identificatore di localizzazione della lingua.

</dd> <dt>

*ppCardNames* \[ Cambio\]
</dt> <dd>

Puntatore a un SAFEARRAY di BSTR che contiene i nomi delle smart card che hanno soddisfatto i parametri di ricerca in caso di esito positivo; **NULL se** l'operazione non è riuscita.

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

Per recuperare tutti i [*lettori o*](../secgloss/r-gly.md) i [*reader noti,*](../secgloss/r-gly.md)chiamare [**rispettivamente ListReaders**](iscarddatabase-listreaders.md) o [**ListReaderGroups.**](iscarddatabase-listreadergroups.md)

Per recuperare [*rispettivamente il servizio*](../secgloss/p-gly.md) primario o le interfacce di una scheda specifica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces.**](iscarddatabase-listcardinterfaces.md)

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare i smart card che corrispondono alla stringa ATR specificata.


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
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

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReader**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
