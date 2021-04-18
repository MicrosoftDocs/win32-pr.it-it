---
description: Recupera una stringa ATR della smart card.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Metodo IsValid:: get_Atr (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317065"
---
# <a name="iscardget_atr-method"></a>Metodo IsValid:: Get \_ ATR

\[Il metodo **get \_ ATR** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **get \_ ATR** recupera una [*stringa ATR*](../secgloss/a-gly.md) della [*Smart Card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAtr* \[ out\]
</dt> <dd>

Puntatore a un buffer di byte sotto forma di [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) che conterrà la stringa ATR al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppAtr* non è valido.<br/>           |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppAtr*.<br/>          |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria per soddisfare la richiesta non è disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare la stringa ATR dalla smart card.


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
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
| IID<br/>                      | La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ottenere \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ottenere il \_ contesto**](iscard-get-context.md)
</dt> <dt>

[**ottenere il \_ protocollo**](iscard-get-protocol.md)
</dt> <dt>

[**ottenere \_ lo stato**](iscard-get-status.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> <dt>

[**IByteBuffer:: Read**](ibytebuffer-read.md)
</dt> </dl>

 

 
