---
title: Controllo della versione di Windows
description: La versione del sistema operativo è stata incrementata con Windows 10 versione del sistema operativo.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007881"
---
# <a name="windows-version-check"></a>Controllo della versione di Windows

La versione del sistema operativo è stata incrementata con Windows 10 versione del sistema operativo. Ciò significa che anche il numero di versione interno Windows 10 è stato modificato in 10.0. Come in passato, Microsoft si impegna al massimo per mantenere la compatibilità di applicazioni e dispositivi dopo un cambiamento di versione del sistema operativo. Per la maggior parte delle categorie di app (senza dipendenze del kernel), la modifica non influisce negativamente sulla funzionalità dell'app e le app esistenti continueranno a funzionare correttamente Windows 10.

## <a name="manifestations"></a>Manifestazioni

Gli effetti di questa modifica dipendono dalle app. Questo significa che le app che controllano in modo specifico la versione del sistema operativo otterranno un numero di versione superiore, con queste possibili conseguenze:

-   È possibile che i programmi di installazione delle app non riescano a installare le app e che le app non si avviino.
-   Le app potrebbero diventare instabili o subire arresti anomali.
-   Le app potrebbero generare messaggi di errore, ma continuare a funzionare correttamente.

Alcune app eseguono un controllo della versione e si limitano a inviare un avviso agli utenti. Esistono tuttavia alcune app strettamente vincolate al controllo della versione (nei driver o in modalità kernel per evitare il rilevamento). In questi casi, si verifica un errore dell'app se viene rilevata una versione errata. Invece del controllo della versione, è consigliabile uno degli approcci seguenti:

-   Se l'app dipende da funzionalità API specifiche, assicurati di usare come destinazione la versione dell'API corretta.
-   Il numero di versione NTDDI (NT Device Driver Interface) verrà incrementato solo se la funzionalità di destinazione nell'API cambia. Assicurarsi di rilevare la modifica tramite APISet o un'altra API esposta creata dal team delle funzionalità e di non usare la versione come proxy per alcune funzionalità o correzioni. Se sono presenti modifiche importanti e non viene esposto un controllo appropriato, si tratta di un bug.
-   Assicurarsi che l'app NON controlli la versione in modi diversi, ad esempio tramite il Registro di sistema, le versioni dei file, gli offset, la modalità kernel, i driver o altri mezzi. Se l'app deve assolutamente controllare la versione, usare le API GetVersion, che devono restituire il numero principale, secondario e di build.
-   Se si usa l'API GetVersion o altre funzioni dell'helper versione, ad esempio [VerifyVersionInfo,](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)tenere presente che il comportamento di questa API è cambiato a partire da Windows 8.1. Per altri [dettagli, vedere la documentazione dell'API.](../SysInfo/version-helper-apis.md)
-   Se si è proprietari di app come antimalware o firewall, è consigliabile usare i consueti canali di feedback e il programma Insider Windows insider.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>Dichiarazione della Windows 10 con un manifesto dell'app

Se l'app è compatibile con Windows 10, può dichiarare questo fatto nel manifesto [dell'app (eseguibile)](/windows/compatibility/application-executable-manifest) per l'eseguibile dell'app. Ciò indica al sistema che l'app è in grado di comprendere il numero di versione del sistema di Windows 10 10.0 (quindi l'API GetVersion non restituisce una versione precedente) e consente al sistema di disattivare altri comportamenti di compatibilità applicati alle app che non dichiarano la compatibilità Windows 10.

Per dichiarare la compatibilità di Windows 10 in un manifesto dell'app, è necessario aggiungere una sezione di compatibilità del manifesto, se non ne esiste già una, e quindi aggiungere gli elementi **&lt; supportedOS &gt;** per Windows 10 e tutte le altre versioni di Windows che si vuole dichiarare supportate dall'app. [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility)

L'esempio seguente mostra un file manifesto dell'app per un'app che supporta tutte le versioni di Windows da Windows Vista a Windows 10:

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La riga sopra contrassegnata `* ADD THIS LINE *` mostra come definire in modo accurato come destinazione l'applicazione per Windows 10.

La dichiarazione del supporto Windows 10 nel manifesto dell'app non avrà alcun effetto quando si esegue l'app nei sistemi operativi precedenti.

## <a name="resources"></a>Risorse

-   [Application Compatibility Toolkit Download: scaricare il Windows ADK per Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API degli helper versione](../sysinfo/version-helper-apis.md)