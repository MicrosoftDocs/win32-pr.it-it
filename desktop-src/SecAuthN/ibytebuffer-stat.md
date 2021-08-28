---
description: Il metodo Stat recupera informazioni statistiche dall'oggetto flusso.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: Metodo IByteBuffer::Stat (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dd80b408765985b2e009b2e580eb1bf81b08cb5ea1f2e7aaa5ed628a76073a27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127401"
---
# <a name="ibytebufferstat-method"></a>Metodo IByteBuffer::Stat

\[Il **metodo Stat** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo Stat** recupera informazioni statistiche dall'oggetto flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstatstg* \[ Cambio\]
</dt> <dd>

Punta a una **struttura STATSTRUCT** in cui questo metodo inserisce informazioni su questo oggetto flusso. Questo puntatore è **NULL** se si verifica un errore.

</dd> <dt>

*grfStatFlag* \[ Pollici\]
</dt> <dd>

Specifica che questo metodo non restituisce alcuni campi nella struttura **STATSTRUCT,** salvando così un'operazione di allocazione della memoria. I valori vengono prelevati [**dall'enumerazione STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Il **metodo IByteBuffer::Stat** recupera un puntatore alla struttura **STATSTRUCT** che contiene informazioni su questo flusso aperto.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il recupero di informazioni statistiche dal flusso.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

