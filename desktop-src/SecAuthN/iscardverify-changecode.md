---
description: Sostituisce il codice CHV (verifica del contenitore di schede) corrente con il nuovo codice CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Metodo ISCardVerify:: ChangeCode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757019"
---
# <a name="iscardverifychangecode-method"></a>Metodo ISCardVerify:: ChangeCode

\[Il metodo **ChangeCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ChangeCode** sostituisce il codice CHV corrente (verifica del contenitore di schede) con il nuovo codice CHV.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOldCode* \[ in\]
</dt> <dd>

Puntatore a un [**IByteBuffer**](ibytebuffer.md) contenente il codice corrente dell'utente.

</dd> <dt>

*pNewCode* \[ in\]
</dt> <dd>

Puntatore a un [**IByteBuffer**](ibytebuffer.md) contenente il nuovo codice che verrà presentato alla [*Smart Card*](../secgloss/s-gly.md) durante il processo di modifica per autenticare l'utente.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Indica se il codice è globale o locale e se il codice deve essere abilitato o disabilitato.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ IHV \_ globale**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ IHV \_ locale**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**\_ \_ Abilitazione SC FL IHV \_**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**SC \_ FL \_ IHV \_ disabilitata**
</dt> </dl> </dd> <dt>

*lRef* \[ in\]
</dt> <dd>

Riferimento specifico per smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



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

[**IByteBuffer**](ibytebuffer.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[Valori restituiti da Smart Card](authentication-return-values.md)
</dt> </dl>

 

 
