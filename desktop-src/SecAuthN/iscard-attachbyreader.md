---
description: Il metodo AttachByReader apre la smart card nel lettore denominato.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'Metodo IsValid:: AttachByReader (Scardmgr. h)'
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
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968292"
---
# <a name="iscardattachbyreader-method"></a>Metodo IsValid:: AttachByReader

\[Il metodo **AttachByReader** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **AttachByReader** apre la [*Smart Card*](../secgloss/s-gly.md) nel [*lettore*](../secgloss/r-gly.md)denominato.

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

*bstrReaderName* \[ in\]
</dt> <dd>

**BSTR** che contiene il nome del lettore di smart card.

</dd> <dt>

*SHAREMODE* \[ in\]
</dt> <dd>

Modalità in cui richiedere l'accesso alla smart card.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ESCLUSIVO**</dt> </dl> | Nessun altro usa questa connessione alla smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**CONDIVISO**</dt> </dl>          | Questa connessione può essere utilizzata da altre applicazioni.<br/>        |



 

</dd> <dt>

*PrefProtocol* \[ in\]
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
| <dl> <dt>**\_OK**</dt> </dl>         | L'apertura della smart card nel lettore denominato è stata completata correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si è verificato un problema con uno o più parametri passati nella funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

Al termine dell'utilizzo del lettore, rilasciare l'allegato chiamando il metodo [**etach::D**](iscard-detach.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la connessione a una smart card in un lettore di smart card specificato.


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

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Scollegare**](iscard-detach.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> <dt>

[**Ricollegare**](iscard-reattach.md)
</dt> </dl>

 

 
