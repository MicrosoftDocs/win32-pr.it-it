---
description: Internet Explorer 8 - Protezione esecuzione dati/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8 - Protezione esecuzione dati/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1f969aa2e934f36142995150b6484dad2fa5067f6cbb5ab3a947055af375ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998891"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8 - Protezione esecuzione dati/NX

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 abiliterà la protezione DEP/NX quando viene eseguita in un sistema operativo con il Service Pack più recente. Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 e Windows Server 2008 hanno tutti DEP/NX abilitati per impostazione predefinita in Internet Explorer 8.

 

## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Bassa  

> [!Note]  
> In genere, tutte le applicazioni che vengono Internet Explorer e non sono compatibili con DEP/NX si arresteranno in modo anomalo all'avvio e non funzioneranno. Internet Explorer arresto anomalo all'avvio se sono installati componenti aggiuntivi non compatibili con DEP/NX.

 

## <a name="description"></a>Descrizione

DEP/NX è una funzionalità di sicurezza che consente di attenuare le vulnerabilità correlate alla memoria. A Internet Explorer 8, tutti Internet Explorer processi abilitano la funzionalità DEP/NX per impostazione predefinita.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

Il Windows kernel monitora l'esecuzione di un programma. Se il kernel rileva un tentativo di eseguire codice da una pagina di memoria non contrassegnata come eseguibile, il kernel interrompe l'esecuzione del programma, causando un "arresto anomalo". Si tratta di una misura di sicurezza per garantire che le vulnerabilità correlate alla memoria(ad esempio, gli overflow del buffer) nell'applicazione non siano sfruttate per eseguire codice arbitrario.

## <a name="end-user-mitigation"></a>End-User mitigazione

-   Installare una versione successiva del componente aggiuntivo o del framework compatibile con DEP/NX.
-   Eseguire Internet Explorer con privilegi elevati come amministratore e quindi disabilitare DEP/NX usando la casella di controllo Abilita protezione della memoria per attenuare gli attacchi **online** nella scheda **Opzioni Internet**  /   avanzate .

## <a name="developer-solution"></a>Soluzione per sviluppatori

Compilare applicazioni usando le versioni più recenti dei framework compatibili con DEP.

## <a name="leveraging-feature-capabilities"></a>Sfruttare le funzionalità delle funzionalità

-   Usare l'opzione del linker /NXCOMPAT per indicare la compatibilità DEP/NX
-   Optare per il codice in altre difese disponibili, ad esempio la difesa dello stack (/GS), la gestione sicura delle eccezioni (/SafeSEH) e ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

-   Testare il codice con DEP/NX abilitato usando la versione più recente Internet Explorer versione Windows Vista SP1 o versione successiva.
-   Testare con Internet Explorer 7 in Windows Vista dopo aver abilitato l'opzione DEP/NX. Per abilitare DEP/NX per Internet Explorer 7, eseguire Internet Explorer come amministratore, quindi impostare la casella di controllo appropriata nella scheda Strumenti > Opzioni Internet > Avanzate.
-   Eseguire lo Internet Explorer Compatibility Test Tool (IECTT), fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi potenziali dovuti alle modifiche DEP/NX.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Internet Explorer 8 Security Part I: DEP/NX Memory Protection](/archive/blogs/ie/)
-   [Protezione esecuzione programmi](../memory/data-execution-prevention.md)
-   [Nuove API NX aggiunte a Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Compatibilità delle applicazioni Toolkit download](/windows-hardware/get-started/adk-install)
-   [Problemi noti Internet Explorer funzionalità di sicurezza](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
