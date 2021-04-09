---
description: L'esperto deve implementare la funzione Run. Network Monitor chiama la funzione Run per avviare l'esperto nella DLL Expert.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Funzione di callback Run (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879542"
---
# <a name="run-callback-function"></a>Funzione di callback Run

L'esperto deve implementare la funzione **Run** . Network Monitor chiama la funzione **Run** per avviare l'esperto nella dll Expert.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco dell'esperto che viene passato di nuovo a tutte le funzioni di Network Monitor specifiche dell'esperto.

> [!Note]  
> L'identificatore *hExpertKey* può passare una chiave esperta diversa dalla chiave Expert passata dalla funzione [**Configure**](configure.md) .

 

</dd> <dt>

*pConfig* \[ in\]
</dt> <dd>

Puntatore alla configurazione esistente. Il parametro *pConfig* può essere **null** , che significa che l'esperto può essere eseguito con valori predefiniti hardcoded o informazioni di avvio a cui fa riferimento il parametro *pExpertStartupInfo* .

</dd> <dt>

*pExpertStartupInfo* \[ in\]
</dt> <dd>

Puntatore all'elemento Capture che ha lo stato attivo all'avvio dell'esperto.

</dd> <dt>

*StartupFlags* \[ in\]
</dt> <dd>

Indicatore del modo in cui l'esperto deve utilizzare il parametro *pExpertStartupInfo* .

L'unico flag definito è:



| Valore                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**\_flag di avvio esperto usare i dati di \_ \_ \_ avvio \_ \_ sui dati di \_ configurazione \_ .**</dt> </dl> | Questo flag indica che l'esperto usa il parametro *pExpertStartupInfo* e non usa il parametro *pConfig* . In genere, è possibile impostare questo flag quando l'esperto può iniziare con un clic con il pulsante destro del mouse. Se il flag non è impostato, possono verificarsi le due operazioni seguenti: l'esperto non inizia con un clic con il pulsante destro del mouse oppure l'esperto inizia con un clic con il pulsante destro del mouse e quindi l'utente lo configura.<br/> |



 

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Il parametro *HWND* dell'elemento padre (in genere l'interfaccia utente Network Monitor).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se l'esperto inizia, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Durante l'esecuzione, l'esperto esegue il ciclo dei frame nel file di acquisizione e genera un report o crea eventi che mostrano problemi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




