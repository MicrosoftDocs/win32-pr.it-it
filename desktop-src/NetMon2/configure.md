---
description: Configura l'esperto nella DLL di esperti.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configura funzione di callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311630"
---
# <a name="configure-callback-function"></a>Configura funzione di callback

La funzione **Configure** configura l'esperto nella dll Expert.

L'esperto deve implementare la funzione **Configure** . Quando viene ricevuta la chiamata di funzione, l'esperto Visualizza una finestra di dialogo che consente all'utente di modificare qualsiasi elemento configurabile.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hExpertKey* \[ in\]
</dt> <dd>

Identificatore univoco dell'esperto.

L'identificatore univoco viene passato di nuovo a tutte le funzioni di Network Monitor specifiche dell'esperto. Tenere presente che l'identificatore non può essere la stessa chiave esperta di quella passata alla funzione [**Run**](run.md) . Non archiviare la chiave Expert dalla chiamata **Configure** .

</dd> <dt>

*ppConfig* \[ in uscita\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**EXPERTCONFIG**](expertconfig.md) alla voce.

Dopo una corretta uscita, la struttura [**EXPERTCONFIG**](expertconfig.md) a cui si fa riferimento contiene i nuovi dati di configurazione.

</dd> <dt>

*pExpertStartupInfo* \[ in\]
</dt> <dd>

Puntatore all'elemento Capture con lo stato attivo all'avvio dell'esperto.

</dd> <dt>

*StartupFlags* \[ in\]
</dt> <dd>

Flag che indicano il modo in cui l'esperto deve utilizzare il parametro *pExpertStartupInfo* . L'unico flag definito è **\_ flag di avvio esperto usare i dati di \_ \_ \_ avvio \_ \_ sui \_ \_ dati di configurazione**. Il flag indica che l'esperto utilizzerà il parametro *pExpertStartupInfo* anziché il parametro *ppConfig* passato. In genere, il flag viene impostato quando si avvia l'esperto da un menu di scelta rapida.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre. Utilizzare l'handle per aprire una finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se è presente una configurazione corrente, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Network Monitor chiama la funzione **Configure** con la configurazione corrente dell'esperto, se ne esiste una. L'esperto Visualizza una finestra di dialogo con cui è possibile modificare qualsiasi elemento configurabile.

Quando *ppConfig* viene passato in e Network Monitor non dispone di una configurazione archiviata per l'esperto specificato, il valore del parametro può essere **null**. In questo caso, per aprire la finestra di dialogo la funzione **Configure** presuppone i valori predefiniti hardcoded (oppure usa le informazioni di avvio).

I dati di configurazione possono anche essere **null** quando la funzione **Configure** restituisce e viene passato un **valore null** . Questa situazione si verifica quando Network Monitor non dispone di un valore predefinito archiviato e l'utente preme **Annulla**.

L'inizio della struttura di dati [**EXPERTCONFIG**](expertconfig.md) include una sezione privata che archivia le informazioni sulle dimensioni della struttura. La dimensione della struttura **EXPERTCONFIG** deve includere la lunghezza **DWORD** riservata visualizzata all'inizio della struttura. Se, ad esempio, i dati di configurazione richiedono 20 byte di spazio di archiviazione, allocare 24 byte per archiviare i dati. Se *ppConfig* è **null**, la funzione **Configure** chiama la funzione [**ExpertAllocMemory**](expertallocmemory.md) per allocare una nuova configurazione con le dimensioni corrette. Se il buffer non è sufficiente per conservare i dati esperti, l'esperto deve chiamare la funzione [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




