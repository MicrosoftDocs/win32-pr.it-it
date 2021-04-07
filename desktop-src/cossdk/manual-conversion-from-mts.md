---
description: Conversione manuale da MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversione manuale da MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748298"
---
# <a name="manual-conversion-from-mts"></a>Conversione manuale da MTS

Potrebbe essere necessario isolare la conversione dei pacchetti MTS in applicazioni COM+ in modo che si trovino all'esterno del processo di installazione di Windows. La procedura seguente offre un approccio alternativo:

1.  Esportare i pacchetti MTS usando la funzionalità di esportazione del pacchetto MTS 2,0, ottenendo un file di pacchetto MTS e una raccolta di altri file.
2.  Eliminare i pacchetti MTS e aggiornare le finestre oppure eseguire un'installazione pulita di Windows.
3.  Installare i file del pacchetto MTS (. Pak) in un sistema Windows 2000 o versione successiva utilizzando l'installazione guidata dell'applicazione dello strumento di amministrazione Servizi componenti. Sarà inoltre necessario reimpostare l'identità "RunAs" dell'applicazione nel registro di sistema in **HKEY \_ Local \_ Machine \\ software \\ Classes \\ AppID \\ RunAs**.

> [!Note]  
> Solo la procedura di conversione automatica (tramite l'installazione di Windows o l'esecuzione dell'utilità MTSTOCOM) genera il file di log MTSTOCOM. Questo file non viene generato quando si segue la procedura di conversione manuale.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione automatica da MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Risultati e problemi di conversione COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Libreria di amministrazione MTS](mts-administration-library.md)
</dt> </dl>

 

 



