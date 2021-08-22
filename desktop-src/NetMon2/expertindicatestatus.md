---
description: La funzione ExpertIndicateStatus indica la percentuale di completamento dell'analisi degli esperti del file di acquisizione.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Funzione ExpertIndicateStatus (Netmon.h)
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
ms.openlocfilehash: f9f40e339b450496ec4b0aff1f3e951c4d7468fa22f7b2ff3dd2f84de6b92354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012269"
---
# <a name="expertindicatestatus-function"></a>Funzione ExpertIndicateStatus

La **funzione ExpertIndicateStatus** indica la percentuale di completamento dell'analisi del file di acquisizione da parte dell'esperto.

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

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco dell'esperto. Network Monitor passa *hExpertKey* all'esperto quando chiama la [funzione Run.](run.md)

</dd> <dt>

*Stato* \[ Pollici\]
</dt> <dd>

Stato corrente dell'analisi. Specificare uno dei valori [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INACTIVE**</dt> </dl> | L'esperto non è mai iniziato. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**AVVIO \_ DI EXPERTSTATUS**</dt> </dl> | L'esperto sta iniziando. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ IN ESECUZIONE**</dt> </dl>    | L'esperto funziona normalmente. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**PROBLEMA DI STATO \_ ESPERTO**</dt> </dl>    | Un problema specificato nel parametro SubStatus ha arrestato l'esperto. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ ABORTED**</dt> </dl>    | Network Monitor ha arrestato l'esperto. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ DONE**</dt> </dl>             | L'esperto ha completato correttamente l'analisi. <br/>                     |



 

</dd> <dt>

*Stato secondario* \[ Pollici\]
</dt> <dd>

Estensione o chiarimento delle informazioni fornite dal *parametro* Status.

</dd> <dt>

*sztext* \[ Pollici\]
</dt> <dd>

Indicatore di stato del testo facoltativo.

Il valore di questo parametro può **essere NULL.**

</dd> <dt>

*PercentDone* \[ Cambio\]
</dt> <dd>

Percentuale dei dati di acquisizione elaborati dall'esperto.

Quando l'esperto completa correttamente l'analisi di un file di acquisizione, il sistema imposta la percentuale su 100. Qualsiasi numero maggiore di 99 verrà ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è NMERR EXPERT TERMINATE. L'esperto deve eseguire immediatamente la pulizia e restituire il controllo senza \_ \_ completare l'acquisizione.

## <a name="remarks"></a>Commenti

La **funzione ExpertIndicateStatus** può essere chiamata solo da esperti che implementano la [funzione di](run.md) esportazione Run o [Configure.](configure.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
