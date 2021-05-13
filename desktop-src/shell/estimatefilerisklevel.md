---
description: Stima il rischio di esecuzione di codice sconosciuto quando un gestore viene chiamato su un determinato file. Questo rischio si basa su una conoscenza del gestore e del contenuto del codice del file.
title: Funzione EstimateFileRiskLevel
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
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841432"
---
# <a name="estimatefilerisklevel-function"></a>Funzione EstimateFileRiskLevel

\[Questa funzione è disponibile in Windows XP con Service Pack 2 (SP2) tramite Windows Vista. Potrebbe essere stato modificato o non disponibile nelle versioni successive di Windows. Le applicazioni client devono invece usare [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) per presentare un ambiente utente che fornisce download e scambio sicuri di file tramite allegati di posta elettronica e messaggistica.\]

Stima il rischio di esecuzione di codice sconosciuto quando un gestore viene chiamato su un determinato file. Questo rischio si basa su una conoscenza del gestore e del contenuto del codice del file.

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

*pszFilePath* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione Null che contiene il percorso del file sottoposto a controllo rispetto al gestore.

</dd> <dt>

*pszExt* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione Null che contiene l'estensione del file da controllare, con o senza il relativo punto iniziale. Ad esempio, ".txt" o "txt".

</dd> <dt>

*pszHandler* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione Null che contiene il percorso del gestore per il file.

</dd> <dt>

*pfrlEstimate* \[ Cambio\]
</dt> <dd>

Tipo: **LIVELLO DI RISCHIO \_ \_ FILE \***

Quando questa funzione viene restituita correttamente, contiene un puntatore a uno dei valori seguenti che indica il rischio stimato.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ NO \_ OPINION** (0)


</dt> <dd>

Il formato del file non è identificato o il gestore non è identificato. Informazioni insufficienti disponibili per una risposta significativa.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)


</dt> <dd>

Il formato del file è completamente comprensibile, il gestore è noto ed è molto sicuro che non verrà eseguito codice estraneo.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)


</dt> <dd>

Il formato del file è identificato, ma non è sufficientemente comprensibile da etichettare come un rischio elevato o basso.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)


</dt> <dd>

Il formato del file viene riconosciuto e sono stati identificati fattori di rischio elevati.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)


</dt> <dd>

Il formato di file è bloccato in modo specifico per questo gestore.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione non è dichiarata in un'intestazione pubblica o inclusa in un file di libreria. Per usarlo, è necessario caricarlo direttamente dal Winshfhc.dll ordinale 101.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo Windows XP con app desktop SP2 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (versione 5.1 o successiva)</dt> </dl> |



 

 




