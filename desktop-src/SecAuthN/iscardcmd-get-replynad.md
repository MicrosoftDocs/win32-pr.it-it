---
description: Recupera l'indirizzo del nodo (Nad) utilizzato dal smart card nel messaggio di risposta.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: Metodo ISCardCmd::get_ReplyNad (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 22460acc80aae359b3d31a7e4bf592514dd5c559feb68117d7547a0cdbedf144
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577541"
---
# <a name="iscardcmdget_replynad-method"></a>Metodo ISCardCmd::get \_ ReplyNad

\[Il **metodo get \_ ReplyNad** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo get \_ ReplyNad** recupera l'indirizzo del nodo (Nad) usato dal smart card [*nel*](../secgloss/s-gly.md) messaggio di risposta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbNad* \[ Cambio\]
</dt> <dd>

Puntatore al byte che contiene il valore Nad utilizzato dal messaggio di risposta, al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                    | Descrizione                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è stata completata correttamente.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il *parametro pbNad* non è valido.<br/>                     |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Le chiamate interne non sono state in grado di recuperare informazioni nad.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati in precedenza, questo metodo può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare l'indirizzo del nodo (Nad) usato dal [*smart card*](../secgloss/s-gly.md) nel messaggio di risposta. Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza [**dell'interfaccia ISCardCmd.**](iscardcmd.md)


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
