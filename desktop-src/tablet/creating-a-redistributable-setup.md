---
description: Per distribuire un'applicazione abilitata per l'input penna in computer in cui non è in esecuzione Windows Vista o Windows XP Tablet PC Edition 2005 (ovvero i computer che eseguono Windows XP, Windows Server 2003 o Windows 2000), è necessario includere i moduli merge necessari nell'installazione.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Creazione di un'installazione ridistribuibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524385"
---
# <a name="creating-a-redistributable-setup"></a>Creazione di un'installazione ridistribuibile

Per distribuire un'applicazione abilitata per l'input penna in computer in cui non è in esecuzione Windows Vista o Windows XP Tablet PC Edition 2005 (ovvero i computer che eseguono Windows XP, Windows Server 2003 o Windows 2000), è necessario includere i moduli merge necessari nell'installazione.

Il modulo merge Mstpcrt. msm include tutti i file, le risorse, le voci del registro di sistema e la logica di installazione necessari per Windows Installer installare i file condivisi richiesti da altre piattaforme per eseguire applicazioni non gestite sviluppate per il Tablet PC. Mstpcrt. msm viene utilizzato dai file di Windows Installer (MSI). Per le applicazioni che usano l'oggetto [**InkDivider**](inkdivider-class.md) , è anche necessario ridistribuire InkDiv. msm. Per le applicazioni che utilizzano componenti gestiti, è necessario includere anche i file di modulo unione per i componenti gestiti.

Nella tabella seguente vengono descritti i file di modulo unione forniti con il Software Development Kit (SDK) di Windows XP Tablet PC Edition.



| Modulo unione ridistribuibile | Descrizione                                                                                                                    | File                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv. msm<br/>        | Installa la versione non gestita dell'oggetto [**InkDivider**](inkdivider-class.md) .<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt. msm<br/>       | Installa i componenti non gestiti della piattaforma Tablet PC versione 1,0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60. msm<br/>       | Installa i componenti del runtime di Microsoft Visual C++.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt. msm<br/>        | Installa i componenti del runtime di Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17. msm<br/>      | Installa i componenti gestiti del runtime di Tablet PC Platform. Richiede che sia installato il file mstpcrt. msm.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM. msm<br/>         | Installa i componenti di automazione dell'API InkAnalysis.<br/>                                                          | IACom.dll<br/>                                        |
| IACore. msm<br/>        | Installa i componenti della classe base dell'API InkAnalysis.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm. msm<br/>      | Installa i componenti della libreria gestita dell'API InkAnalysis.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX. msm<br/>       | Installa i componenti Windows Presentation Foundation dell'API InkAnalysis.<br/>                                     | IAWinFX.dll<br/>                                      |
| Journal. msm<br/>       | Installa i componenti Reader del journal.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom. msm<br/>        | Installa i componenti di automazione dello spazio dei nomi StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Per utilizzare la funzionalità del Framework Microsoft .NET incluso nei moduli unione per i componenti gestiti, è necessario aver installato il Service Pack 2 del Framework nel computer di destinazione.

 

## <a name="reduced-feature-set"></a>Set di funzionalità ridotto

Le applicazioni abilitate per l'input penna considerano gli eventi del mouse come movimenti penna per simulare l'uso di una penna del tablet. Gli utenti possono aggiungere input penna, cancellare input penna e salvare documenti input penna. Tuttavia, i riconoscimenti e i movimenti non sono disponibili per utenti diversi da quelli che eseguono Windows XP Tablet PC Edition.

Mstpcrt. msm non include il pannello di input di Windows Journal o Tablet PC.

L'oggetto [**PenInputPanel**](peninputpanel-class.md) non funziona in alcun sistema operativo oltre a Windows XP Tablet PC Edition.

## <a name="deployment"></a>Distribuzione

> [!Note]  
> Se l'applicazione usa codice gestito, è necessario distribuire anche il Framework. Il Framework deve essere installato prima dell'installazione degli assembly gestiti di Tablet PC.

 

Per includere Mstpcrt. msm in un progetto di installazione di Microsoft Visual Studio .NET:

1.  Nella Esplora soluzioni selezionare il progetto di installazione.
2.  Scegliere **Aggiungi** dal menu progetto, quindi fare clic su **Merge Module**.
    > [!Note]  
    > Per accedere alla finestra di dialogo **Aggiungi moduli** è inoltre possibile fare clic con il pulsante destro del mouse sul nome del progetto di installazione nell'Esplora soluzioni, scegliere **Aggiungi**, quindi **modulo unione**.

     

3.  Nella finestra di dialogo **Aggiungi moduli** passare a e selezionare **Mstpcrt. msm**.
4.  Fare clic su **Apri**.

Mstpcrt. msm viene aggiunto al progetto di installazione e viene visualizzato nella finestra Esplora soluzioni.

Windows Installer aggiunge i file contenuti nel modulo merge alla cartella Program Files. Per usare questi file, gli utenti finali devono essere connessi con un account che abbia accesso alla cartella Program Files.

> [!Note]  
> È necessario aggiungere le azioni azione [SelfRegModules](../msi/selfregmodules-action.md) e [azione SelfUnregModules](../msi/selfunregmodules-action.md) alla sequenza di installazione. Le azioni azione [MsiPublishAssemblies](../msi/msipublishassemblies-action.md) e [azione MsiUnpublishAssemblies](/windows/desktop/Msi/msiunpublishassemblies-action) ricevono l'ordine nella sequenza di installazione da queste azioni.

 

 

