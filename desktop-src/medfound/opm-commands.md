---
description: Comandi di OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandi di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309067"
---
# <a name="opm-commands"></a>Comandi di OPM

Questa sezione elenca i comandi disponibili per l' [Output Protection Manager](output-protection-manager.md) (OPM).

Per inviare un comando OPM, chiamare [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Per ogni comando vengono elencate le informazioni seguenti.



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID comando | Identifica il comando. Impostare il membro **guidSetting** della struttura di [**configurazione dei \_ \_ parametri di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) uguale a questo valore. |
| Dati di input   | Specifica come interpretare la matrice **abParameters** nella struttura [**dei \_ \_ parametri di configurazione di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .                      |



 

Sono definiti i seguenti comandi:



| Comando                                                                                                       | Descrizione                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA**](opm-set-acp-and-cgmsa-signaling.md)                               | Specifica le informazioni sul segnale video, oltre al livello di protezione.                      |
| [**\_set OPM \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP). |
| [**\_livello di \_ protezione \_ set OPM**](opm-set-protection-level.md)                                               | Imposta il livello di protezione per un meccanismo di protezione dell'output.                                       |
| [**\_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS**](opm-set-protection-level-according-to-css-dvd.md) | Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di OPM](opm-programming-reference.md)
</dt> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 



