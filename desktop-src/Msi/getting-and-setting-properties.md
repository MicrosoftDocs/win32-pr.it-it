---
description: Per usare le proprietà nell'installazione, è possibile ottenere e impostare i valori delle proprietà dai programmi usando MsiGetProperty e MsiSetProperty e includere come parte delle istruzioni condizionali nel database di installazione.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Recupero e impostazione delle proprietà (Windows di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1009fc9370a870c53b3fe5ad471f52dea195648b36bab28dff76fe1271283be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635951"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Recupero e impostazione delle proprietà (Windows di installazione)

Per usare [le](properties.md) proprietà nell'installazione, è possibile ottenere e impostare i valori delle proprietà dai programmi usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) e [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e includere come parte delle istruzioni condizionali nel database di installazione.

-   Per ottenere una proprietà corrente, chiamare la [**funzione MsiGetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)
-   Per ottenere lo stato di installazione corrente, chiamare la [**funzione MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)
-   Per ottenere la lingua per l'installazione corrente, chiamare la [**funzione MsiGetLanguage.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)
-   Per impostare una proprietà, chiamare la [**funzione MsiSetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)
-   Per impostare lo stato di installazione, chiamare [**la funzione MsiSetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)
-   Per cancellare una proprietà (impostandola su Null), impostare il valore della proprietà su una stringa vuota: "".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Cancellazione di una proprietà del programma di installazione](clearing-an-installer-property.md)
</dt> </dl>

 

 



