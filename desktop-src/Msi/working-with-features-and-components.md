---
description: Esistono diverse funzioni che modificano l'installazione dei componenti e delle funzionalità del prodotto. Di seguito viene descritto come modificare funzionalità e componenti.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Uso di funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145174"
---
# <a name="working-with-features-and-components"></a>Uso di funzionalità e componenti

Esistono diverse funzioni che modificano l'installazione di componenti [e funzionalità del prodotto.](components-and-features.md) Di seguito viene descritto come modificare funzionalità e componenti.

**Per modificare l'installazione di funzionalità e componenti**

1.  Impostare il livello di installazione per un componente o una funzionalità chiamando la [**funzione MsiSetInstallLevel.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)

    A ogni funzionalità di un pacchetto viene assegnato un livello di installazione nella [tabella Delle funzionalità](feature-table.md). Se il livello di installazione di una funzionalità è inferiore al livello impostato da [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la funzionalità viene selezionata per l'installazione. Dopo **aver chiamato MsiSetInstallLevel,** è possibile modificare in modo esplicito se una funzionalità è installata.

2.  Determinare gli stati disponibili per una funzionalità specificata chiamando la [**funzione MsiGetFeatureValidStates.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
3.  Ottenere i requisiti di spazio su disco per una funzionalità specificata e le relative funzionalità figlio chiamando la [**funzione MsiGetFeatureCost.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
4.  Ottenere lo stato corrente di una funzionalità o di un componente chiamando la [**funzione MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o [**la funzione MsiGetComponentState.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
5.  Modificare lo stato della funzionalità o del componente con la [**funzione MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o [**la funzione MsiSetComponentState.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)

 

 



