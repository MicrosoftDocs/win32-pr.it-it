---
title: Versioni di XInput
description: XInput è un'API multipiattaforma disponibile per l'uso in Xbox e Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277712308ca6083147d10138ba4d78e7e0fa086df95a78ab2b8317abca567dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430785"
---
# <a name="xinput-versions"></a>Versioni di XInput

XInput è un'API multipiattaforma disponibile per l'uso in Xbox e Windows. In Xbox XInput viene fornito come libreria statica compilata nel file eseguibile principale del gioco. In Windows, XInput viene fornito come DLL installato nelle cartelle di sistema del sistema operativo.

Esistono attualmente tre versioni correnti della DLL XInput. Scegliere la versione appropriata di XInput in base alla funzionalità di XInput in uso e alle versioni di Windows che si intende supportare.

- XInput 1.4: XInput 1.4 viene fornito come parte di Windows 10. Usare questa versione per la creazione di app UWP.
- XInput 9.1.0: XInput 9.1.0 viene fornito come parte di Windows Vista, Windows 7 e Windows 8. Usare questa versione se l'app desktop deve essere eseguita in queste versioni di Windows e si usa la funzionalità XInput di base.
- XInput 1.3: XInput 1.3 viene fornito come componente ridistribuibile in DirectX SDK con supporto per Windows Vista, Windows 7 e Windows 8. Usare questa versione se l'app desktop deve essere eseguita in queste versioni di Windows ed è necessaria una funzionalità non supportata da XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1.4

XInput 1.4 viene attualmente fornito come componente di sistema in Windows 8 come XINPUT1 \_4.DLL. È disponibile nella "posta in arrivo" e non richiede la ridistribuzione con un'applicazione. Il Windows Software Development Kit (SDK) contiene l'intestazione e la libreria di importazione per il collegamento statico a XINPUT1 \_4.DLL. Per scaricare l'SDK Windows 8, vedere [Download per lo sviluppo di app desktop.](https://developer.microsoft.com/windows/downloads/)

XInput 1.4 offre questi vantaggi principali rispetto ad altre versioni di XInput:

-   Questa è l'unica versione che può essere usata nelle app C++/DirectX Windows Store.
-   La nuova funzione [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) fornisce una stringa ID dispositivo audio che è possibile usare per aprire un dispositivo audio o voce master XAudio2 per un visore VR collegato a un controller comune Xbox. La [**funzione XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) non è disponibile in questa versione.
-   Offre funzionalità migliorate per la creazione di report sui dispositivi, tra cui \_ XINPUT CAPS \_ WIRELESS, XINPUT \_ CAPS \_ FFB \_ SUPPORTED, XINPUT \_ CAPS \_ PMD SUPPORTED e XINPUT CAPS NO NAVIGATION \_ \_ flags \_ \_ \_ \_ \_ e report più accurati di XINPUT CAPS VOICE SUPPORTED. Questi flag vengono combinati nel **membro Flags** della [**struttura XINPUT \_ CAPABILITIES.**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) La [**funzione XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) restituisce **XINPUT \_ CAPABILITIES**.

### <a name="xinput-910"></a>XInput 9.1.0

Come XInput 1.4, XInput 9.1.0 viene attualmente fornito come componente di sistema in Windows 10, Windows 8.x, Windows 7 e Windows Vista come XINPUT9 \_ 1 \_0.DLL. Viene mantenuto principalmente per garantire la compatibilità con le versioni precedenti delle applicazioni esistenti. Ha un set di funzioni ridotto, quindi è consigliabile usare XInput 1.4, se possibile. È tuttavia utile usare per le applicazioni che devono essere eseguite in versioni di livello inferiore di Windows ma che non necessitano delle funzionalità audio aggiuntive fornite da XInput 1.4 o XInput 1.3.

L Windows SDK contiene l'intestazione e la libreria di importazione per il collegamento statico a XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 presenta questi svantaggi rispetto ad altre versioni di XInput:

-   Per motivi di compatibilità con le versioni precedenti, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) in questa versione di XInput restituisce informazioni sulle funzionalità fisse. Indipendentemente dal dispositivo controller comune Xbox collegato, **XInputGetCapabilities** in XInput 9.1.0 segnala sempre un sottotipo di dispositivo GAMEPAD. Non restituirà il bit di funzionalità XINPUT \_ CAPS \_ WIRELESS anche se un dispositivo wireless è connesso.
-   Non è possibile determinare il visore VR per un DETERMINATO ID utente. La [**funzione XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) non è disponibile e la funzione [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) non restituirà risultati in Windows 8.x o Windows 10.
-   Le [**funzioni XInputEnable,**](/windows/desktop/api/XInput/nf-xinput-xinputenable) [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)e [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) non sono disponibili.

### <a name="xinput-13"></a>XInput 1.3

Alcune versioni precedenti di XInput sono state fornite come DLL ridistribuibili in DirectX SDK. La prima versione ridistribuibile di XInput, XInput 1.1, disponibile nella versione di aprile 2006 di DirectX SDK. L'ultima versione disponibile in DirectX SDK è XInput 1.3, disponibile nella versione di giugno 2010 di DirectX SDK legacy. *DirectX SDK non è più disponibile in Download Microsoft.*

È possibile usare XInput 1.3 per le applicazioni che supportano versioni di livello inferiore di Windows e richiedono funzionalità non fornite da XInput 9.1.0(ovvero, segnalazione sottotipo corretta, supporto audio, supporto esplicito per la segnalazione della batteria e così via).
