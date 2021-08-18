---
description: Specifica l'indirizzo del nodo (Nad) da usare con l'interfaccia ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: Metodo ISCardCmd::p ut_Nad (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 84ade2e2ca69c328650f4c7df485814e4eaacedf3fdb0190fc883cde864a8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481391"
---
# <a name="iscardcmdput_nad-method"></a>Metodo ISCardCmd::p ut \_ Nad

\[Il **metodo \_ put Nad** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo put \_ Nad** specifica l'indirizzo del nodo (Nad) da usare con l'interfaccia [**ISCardCmd.**](iscardcmd.md) Questo vale solo per le comunicazioni che usano le comunicazioni [*del protocollo T=1.*](../secgloss/t-gly.md) Per impostazione predefinita, [**l'oggetto ISCardCmd**](iscardcmd.md) usa un valore Nad pari a zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bNad* \[ Pollici\]
</dt> <dd>

Byte che rappresenta l'oggetto Nad da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | L'operazione è stata completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro bNad* non è valido.<br/>    |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato solo quando è necessario usare un valore diverso da zero per Nad.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come specificare un indirizzo del nodo da usare con [**l'interfaccia ISCardCmd.**](iscardcmd.md) L'esempio presuppone che byNadValue sia una variabile di tipo **BYTE** a cui è stato assegnato in precedenza un valore e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia **ISCardCmd.**


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd è definito come \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
