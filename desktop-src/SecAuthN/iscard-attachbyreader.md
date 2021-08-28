---
description: Il metodo AttachByReader apre il smart card nel lettore denominato.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: Metodo ISCard::AttachByReader (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1227c94edbf5816a8f1e867436462a743e6961e3ca70bb7b8a521c289312f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015681"
---
# <a name="iscardattachbyreader-method"></a>Metodo ISCard::AttachByReader

\[Il **metodo AttachByReader** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo AttachByReader** apre il [*smart card*](../secgloss/s-gly.md) nel lettore [*denominato.*](../secgloss/r-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrReaderName* \[ Pollici\]
</dt> <dd>

Oggetto **BSTR** che contiene il nome del lettore smart card lettura.

</dd> <dt>

*ShareMode* \[ Pollici\]
</dt> <dd>

Modalità in cui richiedere l'accesso al smart card.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Esclusivo**</dt> </dl> | Nessun altro usa questa connessione al smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**condiviso**</dt> </dl>          | Altre applicazioni possono usare questa connessione.<br/>        |



 

</dd> <dt>

*PrefProtocol* \[ Pollici\]
</dt> <dd>

Valore del protocollo preferito.

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | L'apertura nel smart card nel lettore denominato è stata completata correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati [](../secgloss/s-gly.md) in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

Al termine dell'uso del lettore, rilasciare l'allegato chiamando il metodo [**ISCard::D etach.**](iscard-detach.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra il collegamento a un smart card in un lettore smart card specificato.


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
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
| IID<br/>                      | IID ISCard è definito come \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Ricollegare**](iscard-reattach.md)
</dt> </dl>

 

 
