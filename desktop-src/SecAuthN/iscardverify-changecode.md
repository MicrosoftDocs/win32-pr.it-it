---
description: Sostituisce il codice CHV corrente (verifica del titolare della carta) con il nuovo codice CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: Metodo ISCardVerify::ChangeCode
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
ms.openlocfilehash: 665cf0ec4c06feca9bcc221125daedc9ab8a12dabed0577b1f4bab5a31334804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013541"
---
# <a name="iscardverifychangecode-method"></a>Metodo ISCardVerify::ChangeCode

\[Il **metodo ChangeCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ChangeCode** sostituisce il codice CHV corrente (verifica del titolare della carta) con il nuovo codice CHV.

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

*pOldCode* \[ Pollici\]
</dt> <dd>

Puntatore a [**un oggetto IByteBuffer**](ibytebuffer.md) contenente il codice corrente dell'utente.

</dd> <dt>

*pNewCode* \[ Pollici\]
</dt> <dd>

Puntatore a [**un oggetto IByteBuffer**](ibytebuffer.md) contenente il nuovo codice che verrà presentato al smart card [*durante*](../secgloss/s-gly.md) il processo di modifica per autenticare l'utente.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Indica se il codice è globale o locale e se deve essere abilitato o disabilitato.

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

**SC \_ FL \_ IHV \_ GLOBAL**
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

**SC \_ FL \_ IHV \_ LOCAL**
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

**SC \_ FL \_ IHV \_ ENABLE**
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

**SC \_ FL \_ IHV \_ DISABLE**
</dt> </dl> </dd> <dt>

*lRef* \[ Pollici\]
</dt> <dd>

Riferimento specifico della smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify.**](iscardverify.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[Valori restituiti dalla smart card](authentication-return-values.md)
</dt> </dl>

 

 
