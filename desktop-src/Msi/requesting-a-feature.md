---
description: Un'applicazione deve chiamare diverse funzioni per richiedere funzionalità.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Richiesta di una funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288804168f6adf936550fee0ac0c542bd68f4d468d6aedd6372071744b9fec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990561"
---
# <a name="requesting-a-feature"></a>Richiesta di una funzionalità

Un'applicazione deve chiamare diverse funzioni per richiedere funzionalità. Prima di richiedere una funzionalità, l'applicazione deve assicurarsi che la funzionalità sia installata. Se l'applicazione chiama [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) prima che l'applicazione possa accedere a una funzionalità, l'applicazione può usare le informazioni restituite per gestire le metriche di utilizzo.

**Per richiedere una funzionalità**

1.  Chiamare la [**funzione MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se si vuole determinare la disponibilità di una funzionalità senza incrementare il numero di utilizzi.
2.  Indicare la finalità dell'applicazione di usare una funzionalità chiamando la [**funzione MsiUseFeature.**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
3.  Determinare i percorsi dei file chiamando [**la funzione MsiGetComponentPath.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
4.  Configurare la funzionalità chiamando la [**funzione MsiConfigureFeature.**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
5.  Ottenere le metriche di utilizzo che l'applicazione può usare chiamando la [**funzione MsiGetFeatureUsage.**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)

Il diagramma seguente illustra il modello di richiesta di funzionalità.

![modello di richiesta di funzionalità. ](images/over2.png)

 

 



