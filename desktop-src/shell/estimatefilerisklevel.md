---
description: Stima il rischio di eseguire codice sconosciuto quando un gestore viene chiamato su un determinato file. Questo rischio è basato sulla comprensione del gestore e del contenuto del codice del file.
title: EstimateFileRiskLevel (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980487"
---
# <a name="estimatefilerisklevel-function"></a>EstimateFileRiskLevel (funzione)

\[Questa funzione è disponibile in Windows XP con Service Pack 2 (SP2) tramite Windows Vista. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. Le applicazioni client devono invece usare [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) per presentare un ambiente utente che fornisce il download sicuro e lo scambio di file tramite messaggi di posta elettronica e allegati di messaggistica.\]

Stima il rischio di eseguire codice sconosciuto quando un gestore viene chiamato su un determinato file. Questo rischio è basato sulla comprensione del gestore e del contenuto del codice del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszFilePath* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione null che contiene il percorso del file sottoposto a verifica rispetto al gestore.

</dd> <dt>

*pszExt* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione null che contiene l'estensione del file di cui è in corso il controllo, con o senza il relativo punto iniziali. Ad esempio, ". txt" o "txt".

</dd> <dt>

*pszHandler* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione null che contiene il percorso del gestore per il file.

</dd> <dt>

*pfrlEstimate* \[ out\]
</dt> <dd>

Tipo: **\_ \_ \* livello di rischio file* _

Quando questa funzione restituisce correttamente, contiene un puntatore a uno dei valori seguenti che indica il rischio stimato.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ Nessuna \_ opinione** (0)


</dt> <dd>

Il formato del file non è identificato oppure il gestore non è identificato. Informazioni insufficienti disponibili per una risposta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ BASSA** (1)


</dt> <dd>

Il formato del file è completamente comprensibile, il gestore è noto ed è molto sicuro che non verrà eseguito alcun codice estraneo.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERAto** (2)


</dt> <dd>

Il formato del file viene identificato, ma non è sufficientemente comprensibile per l'etichetta come rischio elevato o basso.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ALTA** (3)


</dt> <dd>

Il formato del file è compreso ed è stato identificato un fattore di rischio elevato.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCCO** (4)


</dt> <dd>

Il formato del file è bloccato in modo specifico per questo gestore.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione non è dichiarata in un'intestazione pubblica o inclusa in un file di libreria. Per usarlo, è necessario caricarlo direttamente da Winshfhc.dll in base all'ordinale 101.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (versione 5,1 o successiva)</dt> </dl> |



 

 




