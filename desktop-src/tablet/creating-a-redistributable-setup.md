---
description: Per distribuire un'applicazione abilitata per l'input penna nei computer che non eseguono Windows Vista o Windows XP Tablet PC Edition 2005 , ovvero i computer che eseguono Windows XP, Windows Server 2003 o Windows 2000), è necessario includere i moduli unione necessari nella configurazione.
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: Creazione di un'installazione ridistribuibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bdd63a00f1f4245ea83173e1a7e609094fe30e5357f5e1ebf3d6da63182cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936871"
---
# <a name="creating-a-redistributable-setup"></a>Creazione di un'installazione ridistribuibile

Per distribuire un'applicazione abilitata per l'input penna nei computer che non eseguono Windows Vista o Windows XP Tablet PC Edition 2005 , ovvero i computer che eseguono Windows XP, Windows Server 2003 o Windows 2000), è necessario includere i moduli unione necessari nella configurazione.

Il modulo unione Mstpcrt.msm include tutti i file, le risorse, le voci del Registro di sistema e la logica di installazione necessari al programma di installazione di Windows per installare i file condivisi necessari ad altre piattaforme per eseguire applicazioni non gestite sviluppate per Tablet PC. Mstpcrt.msm viene utilizzato dai file Windows Installer (.msi). Per le applicazioni che usano [**l'oggetto InkDivider,**](inkdivider-class.md) è necessario ridistribuire anche InkDiv.msm. Per le applicazioni che usano componenti gestiti, è necessario includere anche i file del modulo unione per tali componenti gestiti.

La tabella seguente descrive i file del modulo unione forniti con Windows XP Tablet PC Edition Software Development Kit (SDK).



| Modulo merge ridistribuibile | Descrizione                                                                                                                    | File                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv.msm<br/>        | Installa la versione non gestita [**dell'oggetto InkDivider.**](inkdivider-class.md)<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt.msm<br/>       | Installa i componenti non gestiti della piattaforma Tablet PC versione 1.0.<br/>                                            | Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe<br/>   |
| Msvcp60.msm<br/>       | Installa i componenti del Microsoft Visual C++ runtime.<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt.msm<br/>        | Installa i componenti del runtime di Microsoft Visual C.<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17.msm<br/>      | Installa i componenti gestiti del runtime della piattaforma Tablet PC. Richiede l'installazione del file mstpcrt.msm.<br/> | Microsoft.Ink.dll, Microsoft.Ink.resources.dll<br/>   |
| iaCOM.msm<br/>         | Installa i componenti di automazione dell'API InkAnalysis.<br/>                                                          | IACom.dll<br/>                                        |
| iacore.msm<br/>        | Installa i componenti della classe base dell'API InkAnalysis.<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm.msm<br/>      | Installa i componenti della libreria gestita dell'API InkAnalysis.<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX.msm<br/>       | Installa i componenti Windows Presentation Foundation dell'API InkAnalysis.<br/>                                     | IAWinFX.dll<br/>                                      |
| journal.msm<br/>       | Installa i componenti lettore journal.<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom.msm<br/>        | Installa i componenti di automazione dello spazio dei nomi StylusInput.<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> Per utilizzare la funzionalità di Microsoft .NET Framework inclusa nei moduli unione per i componenti gestiti, è necessario aver installato Service Pack 2 di Framework nel computer di destinazione.

 

## <a name="reduced-feature-set"></a>Set di funzionalità ridotto

Le applicazioni abilitate per l'input penna trattano gli eventi del mouse come movimenti della penna per simulare l'uso di una penna da tablet. Gli utenti possono aggiungere input penna, cancellare l'input penna e salvare documenti input penna. Tuttavia, il riconoscimento e i movimenti non sono disponibili per utenti diversi da quelli che eseguono Windows XP Tablet PC Edition.

Mstpcrt.msm non include Windows di input journal o tablet PC.

[**L'oggetto PenInputPanel**](peninputpanel-class.md) non funziona in alcun sistema operativo oltre Windows XP Tablet PC Edition.

## <a name="deployment"></a>Distribuzione

> [!Note]  
> Se l'applicazione usa codice gestito, è necessario distribuire anche framework. Il framework deve essere installato prima dell'installazione degli assembly gestiti di Tablet PC.

 

Per includere Mstpcrt.msm in un progetto Microsoft Visual Studio di installazione di .NET:

1.  Nella finestra Esplora soluzioni selezionare il progetto di installazione.
2.  Scegliere Aggiungi dal menu Project e quindi fare clic su **Merge module (Modulo unione).**
    > [!Note]  
    > È anche possibile visualizzare la **finestra** di dialogo Aggiungi moduli facendo clic con il pulsante destro del mouse sul nome del progetto del programma di installazione nel Esplora soluzioni, scegliendo Aggiungi **e** quindi merge **module (Modulo unione).**

     

3.  Nella finestra **di dialogo** Aggiungi moduli passare a e selezionare **Mstpcrt.msm.**
4.  Fare clic su **Apri**.

Mstpcrt.msm viene aggiunto al progetto di installazione e viene visualizzato nella Esplora soluzioni configurazione.

Windows Il programma di installazione aggiunge i file contenuti nel modulo unione alla cartella Programmi. Per usare questi file, gli utenti finali devono essere connessi con un account che abbia accesso alla cartella Programmi.

> [!Note]  
> È necessario aggiungere [azioni SelfRegModules Action](../msi/selfregmodules-action.md) e [SelfUnregModules Action](../msi/selfunregmodules-action.md) alla sequenza di installazione. Le [azioni Azione MsiPublishAssemblies](../msi/msipublishassemblies-action.md) e [Azione MsiUnpublishAssemblies](/windows/desktop/Msi/msiunpublishassemblies-action) ricevono l'ordine nella sequenza di installazione da queste azioni.

 

 

