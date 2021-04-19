---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-Protezione esecuzione dati/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc73fcd70a244288aceaead426bf09f07656740d
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314774"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8-Protezione esecuzione dati/NX

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows XP, Windows Vista, Windows 7  
**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2  










> [!Note]  
> Internet Explorer 8 Abilita la protezione DEP/NX quando viene eseguita in un sistema operativo con la Service Pack più recente. Per Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 e Windows Server 2008 tutti i programmi DEP/NX sono abilitati per impostazione predefinita in Internet Explorer 8.

 

## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -bassa  

> [!Note]  
> In genere, qualsiasi applicazione eseguita in Internet Explorer e non è compatibile con DEP/NX si arresterà in modo anomalo all'avvio e non funzionerà. Internet Explorer potrebbe arrestarsi in modo anomalo all'avvio se sono installati componenti aggiuntivi che non sono compatibili con DEP/NX.

 

## <a name="description"></a>Descrizione

DEP/NX è una funzionalità di sicurezza che consente di ridurre le vulnerabilità correlate alla memoria. A partire da Internet Explorer 8, tutti i processi di Internet Explorer abilitano la funzionalità DEP/NX per impostazione predefinita.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Il kernel di Windows monitora l'esecuzione di un programma. Se il kernel rileva un tentativo di eseguire codice da una pagina di memoria non contrassegnata come eseguibile, il kernel interrompe l'esecuzione del programma, causando un "arresto anomalo". Si tratta di una misura di sicurezza che consente di garantire che le vulnerabilità correlate alla memoria (ad esempio, gli overflow del buffer) nell'applicazione non possano essere sfruttate per poter eseguire codice arbitrario.

## <a name="end-user-mitigation"></a>Attenuazione End-User

-   Installare una versione più recente del componente aggiuntivo o del Framework compatibile con DEP/NX.
-   Eseguire Internet Explorer con privilegi elevati come amministratore e quindi disabilitare DEP/NX usando la casella **di controllo Abilita protezione della memoria per attenuare gli attacchi online** nella scheda **Opzioni Internet**  /  **Avanzate** .

## <a name="developer-solution"></a>Soluzione per sviluppatori

Compilare applicazioni usando le versioni più recenti dei Framework compatibili con DEP.

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

-   Usare l'opzione del linker/NXCOMPAT per indicare la compatibilità DEP/NX
-   Scegli il codice in altre difese disponibili, ad esempio/GS (stack Defense), gestione eccezioni sicure (/SafeSEH) e ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

-   Testare il codice con DEP/NX abilitato utilizzando la versione più recente di Internet Explorer rilasciata in Windows Vista SP1 o versioni successive.
-   Eseguire un test con Internet Explorer 7 in Windows Vista dopo aver abilitato l'opzione DEP/NX. Per abilitare DEP/NX per Internet Explorer 7, eseguire Internet Explorer come amministratore, quindi impostare la casella di controllo appropriata nella scheda strumenti > Internet opzioni > avanzate.
-   Eseguire lo strumento di test di compatibilità di Internet Explorer (IECTT), fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi causati dalle modifiche DEP/NX.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Sicurezza di Internet Explorer 8 parte I: protezione della memoria DEP/NX](/archive/blogs/ie/)
-   [Protezione esecuzione programmi](../memory/data-execution-prevention.md)
-   [Nuove API NX aggiunte a Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [Download di Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Problemi noti relativi alle funzionalità di sicurezza di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
