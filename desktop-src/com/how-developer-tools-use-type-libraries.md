---
title: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
description: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320196"
---
# <a name="how-developer-tools-use-type-libraries"></a>Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo

Il diagramma seguente illustra il modo in cui i vari strumenti di sviluppo interagiscono con la libreria dei tipi di un oggetto COM. Ogni libreria dei tipi espone interfacce programmatiche standard che possono essere chiamate da strumenti per ottenere informazioni sugli elementi descritti nella libreria dei tipi. In questo diagramma GUID rappresenta l'identificatore univoco globale e la RPC per la chiamata di procedura remota.

![Diagramma che illustra il modo in cui lo strumento di sviluppo interagisce con la libreria dei tipi di un oggetto C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

Nel diagramma precedente, gli strumenti di conversione C++, ad esempio il compilatore MIDL e le procedure guidate fornite dal sistema di sviluppo Microsoft Visual C++, generano file di intestazione e stub. È possibile aggiungere questi file al progetto per utilizzare l'oggetto COM descritto dalla libreria dei tipi.

Analogamente, in Java gli strumenti di sviluppo generano file di classe e di origine Java che è quindi possibile importare nell'applicazione.

In Visual Basic, lo scenario è piuttosto più semplice. Non è necessario generare file aggiuntivi. Nell'ambiente Visual Basic sono disponibili finestre di dialogo che elencano gli oggetti COM attualmente installati nel computer. Si seleziona il componente che si desidera chiamare dall'applicazione e questo viene aggiunto al progetto, come un componente o un riferimento.

Il Visualizzatore OLE-COM legge una libreria dei tipi, genera un file IDL temporaneo basato sulla libreria dei tipi e lo visualizza agli utenti. Nel Visualizzatore OLE-COM viene inoltre visualizzata la sintassi C++ per gli elementi COM elencati nella libreria dei tipi.

Per ulteriori informazioni sulle librerie dei tipi, vedere [librerie dei tipi e il Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 