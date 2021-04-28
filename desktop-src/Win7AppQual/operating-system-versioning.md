---
description: Controllo delle versioni del sistema operativo
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controllo delle versioni del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088039"
---
# <a name="operating-system-versioning"></a>Controllo delle versioni del sistema operativo

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Alta  
**Frequenza** - Alta  









## <a name="description"></a>Descrizione

Il numero di versione interno per Windows 7 e Windows Server 2008 R2 è 6.1. La funzione GetVersion restituirà ora questo numero di versione alle applicazioni quando viene eseguita una query. Ciò è particolarmente importante per AntiVirus, il backup, le applicazioni di utilità e la protezione della copia.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

La manifestazione di questa modifica è specifica dell'applicazione. Ciò significa che qualsiasi applicazione che verifica in modo specifico la versione del sistema operativo otterrà un numero di versione superiore, che può causare una o più delle situazioni seguenti:

-   I programmi di installazione delle applicazioni potrebbero non essere in grado di installare l'applicazione e le applicazioni potrebbero non essere avviate
-   Le applicazioni potrebbero diventare instabili o bloccarsi
-   Le applicazioni potrebbero generare messaggi di errore, ma continuano a funzionare correttamente

## <a name="mitigation"></a>Mitigazione

La maggior parte delle applicazioni funzionerà correttamente in Windows 7 e Windows Server 2008 R2 perché la compatibilità delle applicazioni in Windows 7 e Windows Server 2008 R2 è molto elevata. Tuttavia, Windows 7 e Windows Server 2008 R2 includono un Visualizzazione Compatibilità per i programmi di installazione e le applicazioni che verificano la versione del sistema operativo.

Per abilitare la visualizzazione compatibilità, gli utenti possono fare clic con il pulsante destro del mouse sul collegamento o sul file eseguibile e quindi applicare il Visualizzazione Compatibilità di Windows XP SP2 o Windows Vista dalla scheda Compatibilità. Nella maggior parte dei casi, ciò dovrebbe consentire all'applicazione di funzionare correttamente senza la necessità di apportare modifiche all'applicazione.

I professionisti IT possono anche applicare qualsiasi correzione di compatibilità VersionLie applicabile, usando lo strumento Di amministrazione compatibilità, che viene installato con l'Application Compatibility Toolkit (ACT). Ad esempio, se un'applicazione non funziona perché sta cercando, ma non trova, le informazioni sulla versione di Windows XP® con Service Pack 2 (SP2), è possibile applicare WinXPSP2VersionLie per restituire all'applicazione le informazioni sul numero di versione appropriate, indipendentemente dalla versione effettiva del sistema operativo in esecuzione nel computer. Le correzioni per la compatibilità VersionLie disponibili sono:

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

In genere, le applicazioni non devono eseguire controlli della versione del sistema operativo. Se un'applicazione necessita di una funzionalità specifica, è preferibile provare a trovarla e non riuscire solo se la funzionalità necessaria è mancante. Come minimo, le applicazioni devono accettare sempre numeri di versione maggiori o uguali alla versione minima supportata del sistema operativo. Le eccezioni devono verificarsi solo se è presente un requisito legale, aziendale o del componente di sistema specifico.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Application Compatibility Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
