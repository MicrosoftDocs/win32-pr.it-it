---
description: Applicazione WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Applicazione WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312469"
---
# <a name="wpdservicesapisample-application"></a>Applicazione WpdServicesApiSample

Un servizio del dispositivo è un'estensione di un oggetto funzionale, oltre a raggruppare logicamente le funzionalità del dispositivo, un servizio del dispositivo offre alle applicazioni la possibilità di individuare tali funzionalità a livello di codice.

L'applicazione di esempio WpdServicesApiSample è un'applicazione desktop da riga di comando che è possibile utilizzare per esplorare i servizi dei contatti sui dispositivi collegati al computer. È possibile esplorare questi servizi elencando supportati: formati, eventi, metodi e servizi astratti. È anche possibile usare questa applicazione per recuperare le proprietà in un determinato servizio di contatto e per richiamare i metodi supportati da tale servizio.

Se non si dispone ancora di un dispositivo che supporta i servizi contatti, è comunque possibile eseguire WpdServicesApiSample se si installa prima il WpdServiceSampleDriver incluso in Windows Driver Kit.

L'applicazione di esempio WpdServicesApiSample include i file seguenti:



| **File**                | **Descrizione**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp  | Contiene metodi che enumerano il contenuto di un determinato servizio contatti.                                                                                                                                  |
| ContentProperties. cpp   | Contiene metodi che leggono e scrivono le proprietà in un servizio di contatti specificato.                                                                                                                              |
| ServiceCapabilities. cpp | Contiene i metodi che recuperano i formati, gli eventi e i servizi astratti supportati supportati da un determinato servizio di contatti.                                                                   |
| ServiceEnumeration. cpp  | Contiene le funzioni di supporto che recuperano informazioni sul dispositivo, ad esempio il nome descrittivo del dispositivo o i servizi di contatti supportati.                                                                       |
| ServiceMethods. cpp      | Contiene i metodi che recuperano e richiamano i metodi supportati da un determinato servizio contatti.                                                                                                              |
| stdafx.cpp              | Include i file standard.                                                                                                                                                                              |
| WpdServiceApiSample. cpp | Ospita la funzione di avvio **\_ tmain** , che chiama la funzione **DoMenu** locale che visualizza un elenco di dispositivi e attività disponibili e chiama la funzione appropriata per la selezione di menu dell'utente. |



 


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi](sample.md)
</dt> </dl>

 

 



