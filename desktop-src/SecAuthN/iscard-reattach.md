---
description: Il metodo ReAttach reimposta o reinizializza il smart card.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: Metodo ISCard::ReAttach (Scardmgr.h)
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
ms.openlocfilehash: f28caee7a40574bf7f31fdc4fb55ddd81ea9e22cca12f1664950c96922d50902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482111"
---
# <a name="iscardreattach-method"></a>Metodo ISCard::ReAttach

\[Il **metodo Ricollegare** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ReAttach** reimposta o reinizializza [*l'smart card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShareMode* \[ Pollici\]
</dt> <dd>

Modalità in cui condividere o possedere esclusivamente la connessione al smart card.



| Valore                                                                                                                                            | Significato                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Esclusivo**</dt> </dl> | Nessun altro usa questa connessione al smart card.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**condiviso**</dt> </dl>          | Altre applicazioni possono usare questa connessione.<br/>        |



 

</dd> <dt>

*InitState* \[ Pollici\]
</dt> <dd>

Indica cosa fare con la scheda.



| Valore                                                                                                                                      | Significato                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Lasciare**</dt> </dl>       | Lascia il smart card nello stato [*corrente.*](../secgloss/s-gly.md)<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**Reimpostare**</dt> </dl>       | Reimposta l'smart card su uno stato noto.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | Rimuove l'alimentazione dal smart card.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Espellere**</dt> </dl>       | Espulse il smart card se il lettore ha funzionalità di espulsione.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |



 

## <a name="remarks"></a>Commenti

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la reinizializzazione del smart card.


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

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
