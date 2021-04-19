---
description: Richiede una verifica dell'utente.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Metodo ISCardVerify:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311616"
---
# <a name="iscardverifyverify-method"></a>Metodo ISCardVerify:: Verify

\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **Verify** richiede una verifica dell'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PCode* \[ in\]
</dt> <dd>

Contiene il codice da presentare alla [*Smart Card*](../secgloss/s-gly.md) nel processo di verifica del titolare della scheda (CHV).

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Indica se il codice è globale o locale.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ IHV \_ globale**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ IHV \_ locale**
</dt> </dl> </dd> <dt>

*lRef* \[ in\]
</dt> <dd>

Riferimento specifico per smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo **Verify** restituisce uno dei valori seguenti:



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify**](iscardverify.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
