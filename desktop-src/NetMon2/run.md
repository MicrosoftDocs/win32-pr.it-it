---
description: L'esperto deve implementare la funzione Run. Network Monitor chiama la funzione Run per avviare l'esperto all'interno della DLL esperta.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Eseguire la funzione di callback (Netmon.h)
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
ms.openlocfilehash: e31c5c729bba133fa4c4d3e36bbc54035a274923a03a8718acf05a601192775b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074501"
---
# <a name="run-callback-function"></a>Eseguire la funzione di callback

L'esperto deve implementare **la funzione** Run. Network Monitor chiama la **funzione Run** per avviare l'esperto all'interno della DLL esperta.

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

*hExpertKey* \[ Pollici\]
</dt> <dd>

Identificatore univoco dell'esperto che viene passato a tutte le funzioni di Network Monitor specifiche dell'esperto.

> [!Note]  
> *L'identificatore hExpertKey* può passare una chiave esperta diversa dalla chiave dell'esperto passata [**dalla**](configure.md) funzione Configure.

 

</dd> <dt>

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla configurazione esistente. Il *parametro pConfig* può essere **NULL,** ovvero l'esperto può essere eseguito con impostazioni predefinite hard-coded o informazioni di avvio a cui fa riferimento il *parametro pExpertStartupInfo.*

</dd> <dt>

*pExpertStartupInfo* \[ Pollici\]
</dt> <dd>

Puntatore all'elemento di acquisizione che ha lo stato attivo all'avvio dell'esperto.

</dd> <dt>

*StartupFlags* \[ Pollici\]
</dt> <dd>

Indicatore di come l'esperto deve usare il *parametro pExpertStartupInfo.*

L'unico flag definito è:



| Valore                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**IL \_ FLAG DI AVVIO EXPERT USA I DATI DI AVVIO SUI DATI DI \_ \_ \_ \_ \_ \_ \_ CONFIGURAZIONE.**</dt> </dl> | Questo flag indica che l'esperto usa il *parametro pExpertStartupInfo* e non usa il *parametro pConfig.* In genere, è possibile impostare questo flag quando l'esperto può iniziare da un clic con il pulsante destro del mouse. Se il flag non è impostato, possono verificarsi le due operazioni seguenti: l'esperto non inizia da un clic con il pulsante destro del mouse oppure l'esperto inizia da un clic con il pulsante destro del mouse e quindi l'utente lo configura.<br/> |



 

</dd> <dt>

*hWndParent* \[ Pollici\]
</dt> <dd>

Il *parametro hWnd* dell'elemento padre (in genere Network Monitor'interfaccia utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se l'esperto inizia, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Durante l'esecuzione, l'esperto scorre in ciclo i frame nel file di acquisizione e genera un report o crea eventi che mostrano problemi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




