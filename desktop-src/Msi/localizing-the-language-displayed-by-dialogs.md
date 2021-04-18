---
description: Il servizio Windows Installer utilizza la lingua dell'utente corrente in tutte le finestre di dialogo fino a quando non viene aperto un pacchetto di Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizzazione della lingua visualizzata dalle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314205"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>Localizzazione della lingua visualizzata dalle finestre di dialogo

Il servizio Windows Installer utilizza la lingua dell'utente corrente in tutte le finestre di dialogo fino a quando non viene aperto un pacchetto di Windows Installer. Il Windows Installer determina l'uso di **GetUserDefaultUILanguage**. Quando viene aperto un pacchetto di Windows Installer, il programma di installazione Visualizza i dialoghi usando la lingua del pacchetto, come specificato dalla proprietà di [**Riepilogo del modello**](template-summary.md) .

Per ulteriori informazioni sulla localizzazione della lingua di un pacchetto di Windows Installer, vedere anche [un esempio di localizzazione](a-localization-example.md).

 

 



