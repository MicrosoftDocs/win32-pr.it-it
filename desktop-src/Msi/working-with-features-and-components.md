---
description: Sono disponibili diverse funzioni che modificano l'installazione dei componenti e delle funzionalità del prodotto. Di seguito viene descritto come modificare le funzionalità e i componenti di.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Utilizzo delle funzionalità e dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313778"
---
# <a name="working-with-features-and-components"></a>Utilizzo delle funzionalità e dei componenti

Sono disponibili diverse funzioni che modificano l'installazione dei [componenti e delle funzionalità](components-and-features.md)del prodotto. Di seguito viene descritto come modificare le funzionalità e i componenti di.

**Per modificare l'installazione di funzionalità e componenti**

1.  Impostare il livello di installazione per un componente o una funzionalità chiamando la funzione [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .

    A ogni funzionalità di un pacchetto viene assegnato un livello di installazione nella [tabella delle funzionalità](feature-table.md). Se il livello di installazione di una funzionalità è inferiore al livello impostato da [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la funzionalità viene selezionata per l'installazione. Dopo la chiamata di **MsiSetInstallLevel** , è possibile modificare in modo esplicito se una funzionalità è installata.

2.  Determinare gli stati disponibili per una funzionalità specificata chiamando la funzione [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .
3.  Ottenere i requisiti di spazio su disco per una funzionalità specificata e le relative caratteristiche figlio chiamando la funzione [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .
4.  Ottenere lo stato corrente di una funzionalità o di un componente chiamando la funzione [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .
5.  Modificare lo stato della funzionalità o del componente con la funzione [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .

 

 



