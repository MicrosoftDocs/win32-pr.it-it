---
description: Avvia la procedura guidata Passport se utilizzata con Rundll32.exe.
title: PassportWizardRunDll (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232110"
---
# <a name="passportwizardrundll-function"></a>PassportWizardRunDll (funzione)

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Avvia la procedura guidata Passport se utilizzata con Rundll32.exe.

## <a name="syntax"></a>Sintassi


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndStub* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per una finestra proprietaria. Questo parametro è in genere impostato su **null**.

</dd> <dt>

*hAppInstance* \[ in\]
</dt> <dd>

Tipo: **HINSTANCE**

Handle per il file di libreria, ottenuto come valore restituito da [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("Netplwiz").

</dd> <dt>

*lpszCmdLine* \[ in\]
</dt> <dd>

Tipo: **LPTSTR**

Dati dell'argomento. Questo valore sarà sempre vuoto.

</dd> <dt>

*nCmdShow* \[ in\]
</dt> <dd>

Tipo: **int**

Imposta la modalità di visualizzazione per la finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

La procedura guidata Passport viene utilizzata per ottenere un Passport predefinito per Windows. Un passaporto consente all'utente di accedere in modo personalizzato a tutti i siti Web di MSN e ad altri siti abilitati per Passport usando l'indirizzo di posta elettronica dell'utente. L'uso di **PassportWizardRunDll** come punto di ingresso nel file Netplwiz.dll tramite un comando rundll32 consente di avviare la procedura guidata Passport da una riga di comando come se si trattasse di un file eseguibile.

**PassportWizardRunDll** viene usato esclusivamente nel contesto di un comando Rundll32.exe come indicato di seguito:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

L'uso di una funzione del punto di ingresso con Rundll32.exe non è simile a una normale chiamata di funzione. Il nome della funzione e il nome del file con estensione dll in cui è archiviato vengono utilizzati solo come parametri della riga di comando. La definizione della funzione mostrata in sintassi è solo un prototipo standard per tutte le funzioni che è possibile chiamare usando rundll32. I valori specifici per *hwndStub*, *hAppInstance* e *nCmdShow* non vengono forniti dall'utente, ma vengono gestiti dietro le quinte da rundll32. **PassportWizardRunDll** non utilizza il valore *lpszCmdLine* , pertanto non sono necessari dati aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (versione 5,60 o successiva)</dt> </dl> |



 

 
