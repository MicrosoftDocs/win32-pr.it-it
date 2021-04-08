---
description: Specifica l'indirizzo del nodo (NAD) da usare con l'interfaccia ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: metodo:p ut_Nad (Scarddat. h)'
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
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879909"
---
# <a name="iscardcmdput_nad-method"></a>ISCardCmd::p \_ Metodo UT nad

\[Il metodo **put \_ nad** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **put \_ nad** specifica l'indirizzo del nodo (NAD) da usare con l'interfaccia [**ISCardCmd**](iscardcmd.md) . Questo vale per le comunicazioni usando solo le comunicazioni di [*protocollo T = 1*](../secgloss/t-gly.md) . Per impostazione predefinita, l'oggetto [**ISCardCmd**](iscardcmd.md) usa un valore nad pari a zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bNad* \[ in\]
</dt> <dd>

Byte che rappresenta il nad da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *bNad* non è valido.<br/>    |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato solo quando è necessario usare un valore diverso da zero per il nad.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come specificare un indirizzo di nodo da utilizzare con l'interfaccia [**ISCardCmd**](iscardcmd.md) . Nell'esempio si presuppone che byNadValue sia una variabile di tipo **byte** a cui è stato precedentemente assegnato un valore e che pISCardCmd è un puntatore valido a un'istanza dell'interfaccia **ISCardCmd** .


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
