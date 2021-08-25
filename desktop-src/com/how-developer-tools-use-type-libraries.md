---
title: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
description: Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e829459176d96beab3fd818b7bafe3cddfb7969ff46531d26709ef6391ecc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993076"
---
# <a name="how-developer-tools-use-type-libraries"></a>Utilizzo delle librerie dei tipi da parte degli strumenti di sviluppo

Il diagramma seguente illustra l'interazione dei vari strumenti di sviluppo con la libreria dei tipi di un oggetto COM. Ogni libreria dei tipi espone interfacce standard a livello di codice che gli strumenti possono chiamare per ottenere informazioni sugli elementi descritti in tale libreria dei tipi. In questo diagramma GUID è l'acronimo di Globally Unique Identifier e RPC per la chiamata di procedura remota.

![Diagramma che illustra l'interazione degli strumenti di sviluppo con la libreria dei tipi di un oggetto C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

Nel diagramma precedente gli strumenti di conversione C++, ad esempio il compilatore MIDL e le procedure guidate fornite dal sistema di sviluppo Microsoft Visual C++, generano file di intestazione e stub. È possibile aggiungere questi file al progetto per usare l'oggetto COM descritto dalla libreria dei tipi.

Analogamente, in Java gli strumenti di sviluppo generano file di classe e di origine Java, che è quindi possibile importare nell'applicazione.

In Visual Basic, lo scenario è un po' più semplice. Non è necessario generare file aggiuntivi. L'Visual Basic fornisce finestre di dialogo che elencano gli oggetti COM attualmente installati nel computer. Si seleziona il componente che si vuole chiamare dall'applicazione e questo viene aggiunto al progetto, come componente o come riferimento.

Il visualizzatore OLE-COM legge una libreria dei tipi, genera un file IDL temporaneo basato sulla libreria dei tipi e lo visualizza agli utenti. Il visualizzatore OLE-COM visualizza anche la sintassi C++ per gli elementi COM elencati nella libreria dei tipi.

Per altre informazioni sulle librerie dei tipi, vedere [Librerie dei tipi e Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 