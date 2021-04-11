---
description: La funzione ExpertIndicateStatus indica la percentuale di completamento dell'analisi degli esperti del file di acquisizione.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Funzione ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128355"
---
# <a name="expertindicatestatus-function"></a>ExpertIndicateStatus (funzione)

La funzione **ExpertIndicateStatus** indica la percentuale di completamento dell'analisi del file di acquisizione da parte dell'esperto.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .

</dd> <dt>

*Stato* \[ di in\]
</dt> <dd>

Stato corrente dell'analisi. Specificare uno dei valori [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INattivo**</dt> </dl> | L'esperto non è mai stato avviato. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**avvio di EXPERTSTATUS \_**</dt> </dl> | L'esperto si sta avviando. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ in esecuzione**</dt> </dl>    | L'esperto viene eseguito normalmente. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**\_problema EXPERTSTATUS**</dt> </dl>    | Un problema specificato nel parametro SubStatus ha interrotto l'esperto. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ interrotto**</dt> </dl>    | Network Monitor arrestato l'esperto. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ completato**</dt> </dl>             | L'analisi è stata completata correttamente. <br/>                     |



 

</dd> <dt>

*Stato secondario* \[ in\]
</dt> <dd>

Estensione o chiarimento delle informazioni fornite dal parametro *status* .

</dd> <dt>

*szText* \[ in\]
</dt> <dd>

Indicatore di stato del testo facoltativo.

Il valore di questo parametro può essere **null**.

</dd> <dt>

*PercentDone* \[ out\]
</dt> <dd>

Percentuale dei dati di acquisizione elaborati dall'esperto.

Quando l'esperto completa correttamente l'analisi di un file di acquisizione, il sistema imposta la percentuale su 100. Qualsiasi numero maggiore di 99 verrà ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è NMERR \_ Expert \_ Terminate; l'esperto deve immediatamente pulire e restituire senza completare l'acquisizione.

## <a name="remarks"></a>Commenti

La funzione **ExpertIndicateStatus** può essere chiamata solo da esperti che implementano la funzione di esportazione [Run](run.md) o [Configure](configure.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
