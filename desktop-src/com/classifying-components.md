---
title: Classificazione di componenti
description: Classificazione di componenti
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856617"
---
# <a name="classifying-components"></a>Classificazione di componenti

Mentre un client è in grado di scorrere l'elenco dei CLSID nel registro di sistema e di selezionare un componente da usare, il caricamento di ogni componente nel registro di sistema e l'esecuzione di query per le interfacce supportate sono molto dispendiosi in termini di tempo. Per determinare se un componente supporta le interfacce necessarie prima di creare un'istanza del componente, è stato sviluppato un metodo per classificare i componenti in categorie.

Una categoria di componenti è un set di interfacce a cui è stato assegnato un GUID denominato CATId. I componenti che implementano tutte le interfacce in una categoria di componenti si registrano come membri di tale categoria di componenti. I componenti che appartengono a una determinata categoria di componenti possono quindi essere selezionati dal registro di sistema. Registrandosi come membro di una categoria di componenti, il componente garantisce che supporti tutte le interfacce membro nella categoria Component.

Un componente può essere un membro di molte categorie. Non è limitato al supporto delle interfacce in una categoria di componenti. Può supportare qualsiasi interfaccia, oltre a quelle presenti in una categoria di componenti.

Diversamente dalla registrazione standard dei componenti, in cui gli sviluppatori devono scrivere codice che registri manualmente gli oggetti, le categorie di componenti automatizzano la maggior parte di queste operazioni. I sei metodi dell'interfaccia [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definiscono le categorie di componenti e registrano gli oggetti che implementano o li richiedono. L'oggetto di [gestione delle categorie di componenti](the-component-categories-manager.md) implementa questa interfaccia. Per ulteriori informazioni sull'utilizzo delle categorie di componenti, vedere **ICatRegister** e [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 




