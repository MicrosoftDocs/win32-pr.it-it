---
description: I GUID della classe di manipolazione diretta seguenti sono definiti in DirectManipulation. idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUID di manipolazione diretta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303942"
---
# <a name="direct-manipulation-guids"></a>GUID di manipolazione diretta

I GUID della classe di [manipolazione diretta](direct-manipulation-portal.md) seguenti sono definiti in DirectManipulation. idl.

- [Master Class-ID](#master-class-ids)
- [Classe di contenuto secondaria-ID](#secondary-content-class-ids)
- [Classe degli oggetti Behavior-ID](#behavior-objects-class-ids)
- [Argomenti correlati](#related-topics)

## <a name="master-class-ids"></a>Master Class-ID

| GUID                                     | Descrizione                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Classe DirectManipulationManager. Questo oggetto fornisce l'accesso a tutte le funzionalità di [manipolazione diretta](direct-manipulation-portal.md) e le API disponibili per l'applicazione.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Classe DCompManipulationCompositor. Si tratta di un'implementazione di [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) che esegue il wrapping di DirectComposition. Tramite questo oggetto compositor DirectManipulation può applicare l'output impostando le trasformazioni direttamente nell'albero DComp. |

## <a name="secondary-content-class-ids"></a>Classe di contenuto secondaria-ID

| GUID                                  | Descrizione                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **\_VERTICALINDICATORCONTENT CLSID**   | Indicatore di panning verticale. Elemento visivo che mostra la posizione corrente nel contenuto che si estende verticalmente all'esterno dello schermo.     |
| **\_HORIZONTALINDICATORCONTENT CLSID** | Indicatore di panning orizzontale. Elemento visivo che mostra la posizione corrente nel contenuto che si estende orizzontalmente fuori schermo. |
| **\_VIRTUALVIEWPORTCONTENT CLSID**     | Viewport virtuale. Un viewport virtuale può essere usato per rispettare gli elementi di posizione fissa per i viewport con lo zoom configurato.          |

## <a name="behavior-objects-class-ids"></a>Classe degli oggetti Behavior-ID

| GUID                                     | Descrizione                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DRAGDROPCONFIGURATIONBEHAVIOR CLSID** | Trascinare & comportamento di rilascio. Consente di selezionare e trascinare gli elementi.                                                                                       |
| **\_AUTOSCROLLBEHAVIOR CLSID**            | Comportamento scorrimento automatico. Consente al contenuto di scorrere automaticamente mentre si avvicina al limite di un asse specificato.                                           |
| **\_DEFERCONTACTSERVICE CLSID**           | Comportamento di rinvio del contatto. Intervallo di tempo (in millliseconds) di attesa prima di chiamare il [**secontatto**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Argomenti correlati

[Manipolazione diretta](direct-manipulation-portal.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**AddConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration), [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
