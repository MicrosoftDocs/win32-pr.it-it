---
description: Avvia la Procedura guidata Passport quando viene usata con Rundll32.exe.
title: Funzione PassportWizardRunDll
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
ms.openlocfilehash: 7b75f4f3371814d00cf5b58dc12854763318c7ee424f35c7a7e6dad9f7734058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820621"
---
# <a name="passportwizardrundll-function"></a>Funzione PassportWizardRunDll

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Avvia la Procedura guidata Passport quando viene usata con Rundll32.exe.

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

*hwndStub* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per una finestra proprietaria. Questo parametro è in genere impostato su **NULL.**

</dd> <dt>

*hAppInstance* \[ Pollici\]
</dt> <dd>

Tipo: **HINSTANCE**

Handle per il file di libreria, ottenuto come valore restituito da [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ Pollici\]
</dt> <dd>

Tipo: **LPTSTR**

Dati dell'argomento. Questo valore sarà sempre vuoto.

</dd> <dt>

*nCmdShow* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Imposta la modalità di visualizzazione per la finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

La procedura guidata Passport viene usata per ottenere un passport predefinito per Windows. Passport consente all'utente di accedere in modo personalizzato a tutti i siti Web MSN e ad altri siti abilitati per Passport usando l'indirizzo di posta elettronica dell'utente. L'uso di **PassportWizardRunDll** come punto di ingresso nel file Netplwiz.dll tramite un comando Rundll32 consente di avviare la Procedura guidata Passport da una riga di comando come se fosse un file eseguibile.

**PassportWizardRunDll** viene usato esclusivamente nel contesto di un comando Rundll32.exe come indicato di seguito:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

L'uso di una funzione del punto Rundll32.exe non è simile a una normale chiamata di funzione. Il nome della funzione e il nome del file .dll in cui è archiviata vengono usati solo come parametri della riga di comando. La definizione di funzione illustrata in Sintassi è solo un prototipo standard per tutte le funzioni che è possibile chiamare usando Rundll32. I valori specifici per *hwndStub*, *hAppInstance* e *nCmdShow* non vengono forniti dall'utente, ma vengono gestiti in background da Rundll32. **PassportWizardRunDll** non usa il valore *lpszCmdLine,* quindi non sono necessari dati aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Nessuno</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (versione 5.60 o successiva)</dt> </dl> |



 

 
