---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controllo delle versioni del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318571"
---
# <a name="operating-system-versioning"></a>Controllo delle versioni del sistema operativo

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -alta  
**Frequenza** -alta  









## <a name="description"></a>Descrizione

Il numero di versione interno per Windows 7 e Windows Server 2008 R2 è 6,1. La funzione GetVersion restituisce ora questo numero di versione alle applicazioni quando viene eseguita una query. Questa operazione è particolarmente importante per l'AntiVirus, il backup, le applicazioni di utilità e la protezione della copia.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

La manifestazione di questa modifica è specifica dell'applicazione. Ciò significa che qualsiasi applicazione che verifica in modo specifico la versione del sistema operativo otterrà un numero di versione superiore, che può causare una o più delle situazioni seguenti:

-   I programmi di installazione delle applicazioni potrebbero non essere in grado di installare l'applicazione e le applicazioni potrebbero non essere in grado di avviarsi
-   Le applicazioni potrebbero diventare instabili o arrestarsi
-   Le applicazioni possono generare messaggi di errore, ma continuare a funzionare correttamente

## <a name="mitigation"></a>Strategia di riduzione del rischio

La maggior parte delle applicazioni funziona correttamente in Windows 7 e Windows Server 2008 R2 perché la compatibilità delle applicazioni in Windows 7 e Windows Server 2008 R2 è molto elevata. Tuttavia, Windows 7 e Windows Server 2008 R2 includono una visualizzazione di compatibilità per i programmi di installazione e le applicazioni che controllano la versione del sistema operativo.

Per abilitare la visualizzazione compatibilità, gli utenti possono fare clic con il pulsante destro del mouse sul collegamento o sul file eseguibile, quindi applicare la visualizzazione compatibilità di Windows XP SP2 o Windows Vista dalla scheda compatibilità. Nella maggior parte dei casi, questa operazione dovrebbe consentire il funzionamento corretto dell'applicazione senza la necessità di apportare modifiche all'applicazione.

I professionisti IT possono inoltre applicare le correzioni di compatibilità di VersionLie applicabili usando lo strumento Compatibility Administrator, che viene installato con Application Compatibility Toolkit (ACT). Se, ad esempio, un'applicazione non riesce a funzionare perché sta controllando, ma non trova, le informazioni sulla versione di Windows XP® con Service Pack 2 (SP2), è possibile applicare WinXPSP2VersionLie per restituire le informazioni sul numero di versione appropriate all'applicazione, indipendentemente dalla versione effettiva del sistema operativo in esecuzione nel computer. Le correzioni di compatibilità di VersionLie disponibili sono:

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Soluzione

In genere, le applicazioni non devono eseguire controlli della versione del sistema operativo. Se un'applicazione necessita di una funzionalità specifica, è preferibile provare a individuare la funzionalità e non riuscire solo se manca la funzionalità necessaria. Come minimo, le applicazioni devono sempre accettare i numeri di versione maggiori o uguali alla versione più bassa supportata del sistema operativo. Le eccezioni dovrebbero verificarsi solo se è presente un requisito specifico per i componenti legali, aziendali o di sistema.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Download di Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
