---
description: I GUID delle classi di manipolazione diretta seguenti sono definiti in DirectManipulation.idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUID di manipolazione diretta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3ee67206bf9395c3a338dba27c9365578d30d7304f465d93fdc90322a77a8a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280542"
---
# <a name="direct-manipulation-guids"></a>GUID di manipolazione diretta

I GUID [delle classi di](direct-manipulation-portal.md) manipolazione diretta seguenti sono definiti in DirectManipulation.idl.

- [ID di classe master](#master-class-ids)
- [ID di classe di contenuto secondario](#secondary-content-class-ids)
- [ID di classe degli oggetti di comportamento](#behavior-objects-class-ids)
- [Argomenti correlati](#related-topics)

## <a name="master-class-ids"></a>ID di classe master

| GUID                                     | Descrizione                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Classe DirectManipulationManager. Questo oggetto fornisce [l'accesso](direct-manipulation-portal.md) a tutte le API e le funzionalità di manipolazione diretta disponibili per l'applicazione.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Classe DCompManipulationCompositor. Si tratta di un'implementazione [**di IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) che esegue il wrapping di DirectComposition. Tramite questo oggetto compositor DirectManipulation può applicare l'output impostando le trasformazioni direttamente nell'albero DComp. |

## <a name="secondary-content-class-ids"></a>ID di classe di contenuto secondario

| GUID                                  | Descrizione                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indicatore di panoramica verticale. Elemento visivo che mostra la posizione corrente nel contenuto che si estende verticalmente all'esterno dello schermo.     |
| **CLSID \_ HorizontalIndicatorContent** | Indicatore di panoramica orizzontale. Elemento visivo che mostra la posizione corrente nel contenuto che si estende orizzontalmente all'esterno dello schermo. |
| **CLSID \_ VirtualViewportContent**     | Viewport virtuale. Un viewport virtuale può essere usato per rispettare gli elementi di posizione fissa per i viewport con zoom configurato.          |

## <a name="behavior-objects-class-ids"></a>ID di classe degli oggetti di comportamento

| GUID                                     | Descrizione                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Trascinare & comportamento di rilascio. Consente di selezionare e trascinare gli elementi.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Comportamento di scorrimento automatico. Consente lo scorrimento automatico del contenuto quando si avvicina al limite di un asse specificato.                                           |
| **CLSID \_ DeferContactService**           | Contattare il comportamento di rinvio. Intervallo di tempo (in millisecondi) di attesa prima di chiamare [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Argomenti correlati

[Manipolazione diretta,](direct-manipulation-portal.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**AddConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration) [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
