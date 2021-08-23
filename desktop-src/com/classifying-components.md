---
title: Classificazione dei componenti
description: Classificazione dei componenti
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e8382c1cbada72c2a8ab480ded78702424736850299b9e5e9fad7b328e3280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048709"
---
# <a name="classifying-components"></a>Classificazione dei componenti

Mentre un client è in grado di esplorare l'elenco di CLSID nel Registro di sistema e selezionare un componente da usare, il caricamento di ogni componente nel Registro di sistema e l'esecuzione di query per le interfacce supportate richiede molto tempo. Per determinare se un componente supporta le interfacce necessarie prima di creare un'istanza del componente, è stato sviluppato un metodo per classificare i componenti in categorie.

Una categoria di componenti è un set di interfacce a cui è stato assegnato un GUID denominato CATID. I componenti che implementano tutte le interfacce in una categoria di componenti si registrano come membri di tale categoria di componenti. I componenti che appartengono a una determinata categoria di componenti possono quindi essere selezionati dal Registro di sistema. Registrando se stesso come membro di una categoria di componenti, il componente garantisce che supporti tutte le interfacce membro nella categoria di componenti.

Un componente può essere membro di molte categorie. Non è limitato al supporto delle interfacce in una categoria di componenti. Può supportare qualsiasi interfaccia, oltre a quelle in una categoria di componenti.

A differenza della registrazione standard dei componenti, in cui gli sviluppatori devono scrivere codice che registra manualmente gli oggetti, le categorie di componenti automatizzano gran parte di questo lavoro. I sei metodi [**dell'interfaccia ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definiscono le categorie di componenti e registrano gli oggetti che le implementano o le richiedono. [L'oggetto Component Categories Manager](the-component-categories-manager.md) implementa questa interfaccia. Per **altre informazioni sull'uso delle categorie** di componenti, vedere ICatRegister e [**ICatInformation.**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 




