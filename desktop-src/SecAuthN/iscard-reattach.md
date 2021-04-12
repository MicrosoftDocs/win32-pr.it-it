---
description: Il metodo di riconnessione Reimposta o reinizializza la smart card.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'Metodo IsValid:: reconnettite (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226605"
---
# <a name="iscardreattach-method"></a>Metodo IsValid:: reconnetti

\[Il metodo di **riconnessione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo di **riconnessione** Reimposta o reinizializza la [*Smart Card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SHAREMODE* \[ in\]
</dt> <dd>

Modalità di condivisione o esclusiva della connessione alla smart card.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ESCLUSIVO**</dt> </dl> | Nessun altro usa questa connessione alla smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**CONDIVISO**</dt> </dl>          | Questa connessione può essere utilizzata da altre applicazioni.<br/>        |



 

</dd> <dt>

*InitState* \[ in\]
</dt> <dd>

Indica le operazioni da eseguire con la scheda.



| Valore                                                                                                                                      | Significato                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**LASCIARE**</dt> </dl>       | Lascia la smart card nello [*stato*](../secgloss/s-gly.md)corrente.<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**REIMPOSTAZIONE**</dt> </dl>       | Reimposta la smart card in uno stato noto.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**Non alimentato**</dt> </dl> | Rimuove l'alimentazione dalla smart card.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**EJECT**</dt> </dl>       | Espelle la smart card se il lettore dispone di funzionalità di espulsione.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si è verificato un problema con uno o più parametri passati nella funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la reinizializzazione della smart card.


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
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

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Scollegare**](iscard-detach.md)
</dt> <dt>

[**Scheda di**](iscard.md)
</dt> </dl>

 

 
