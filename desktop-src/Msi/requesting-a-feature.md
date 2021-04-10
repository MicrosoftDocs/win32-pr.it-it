---
description: Sono disponibili diverse funzioni che devono essere chiamate da un'applicazione per la richiesta di funzionalità.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Richiesta di una funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050252"
---
# <a name="requesting-a-feature"></a>Richiesta di una funzionalità

Sono disponibili diverse funzioni che devono essere chiamate da un'applicazione per la richiesta di funzionalità. Prima di richiedere una funzionalità, l'applicazione deve verificare che la funzionalità sia installata. Se l'applicazione chiama [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) prima che l'applicazione acceda a una funzionalità, l'applicazione può usare le informazioni restituite per mantenere le metriche di utilizzo.

**Per richiedere una funzionalità**

1.  Chiamare la funzione [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se si desidera determinare la disponibilità di una funzionalità senza incrementare il numero di utilizzi.
2.  Indicare la finalità dell'applicazione di usare una funzionalità chiamando la funzione [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .
3.  Determinare i percorsi dei file chiamando la funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .
4.  Configurare la funzionalità chiamando la funzione [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .
5.  Ottenere le metriche di utilizzo che l'applicazione può usare chiamando la funzione [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .

Il diagramma seguente illustra il modello di richiesta di funzionalità.

![modello di richiesta di funzionalità. ](images/over2.png)

 

 



