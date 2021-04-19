---
description: ELS supporta le funzioni definite nella tabella seguente.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funzioni di servizi linguistici estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313833"
---
# <a name="extended-linguistic-services-functions"></a>Funzioni di servizi linguistici estesi

ELS supporta le funzioni definite nella tabella seguente.



| Funzione                                                 | Descrizione                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | Funzione di callback definita dall'applicazione che elabora in modo asincrono i dati prodotti dalla funzione **MappingRecognizeText** .                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | Consente a un servizio ELS di eseguire un'azione dopo il riconoscimento del testo.                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | Libera memoria e risorse allocate durante un'operazione di riconoscimento del testo ELS.                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | Libera la memoria e le risorse allocate per l'applicazione per interagire con uno o più servizi ELS.                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | Recupera un elenco di servizi di supporto della piattaforma ELS disponibili, insieme alle informazioni associate, in base ai criteri specificati dall'applicazione. |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | Chiama un servizio ELS per riconoscere il testo.                                                                                                   |



 

 

 



