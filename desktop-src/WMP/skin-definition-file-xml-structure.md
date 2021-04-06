---
title: Struttura XML del file di definizione dell'interfaccia
description: Struttura XML del file di definizione dell'interfaccia
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- creazione di interfacce, file di definizione dell'interfaccia
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura XML
- Struttura XML per i file di definizione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044980"
---
# <a name="skin-definition-file-xml-structure"></a>Struttura XML del file di definizione dell'interfaccia

Il file di definizione dell'interfaccia è scritto in XML. Una delle principali funzionalità di XML è che è completamente strutturata ed è simile a una struttura. Il codice XML è semplicemente una serie di elementi, ad esempio **View** e **ButtonGroup**. Si inizierà con gli elementi e quindi li si definirà con gli attributi. Nella parte restante di questa esercitazione verranno fornite informazioni dettagliate sugli attributi, ma di seguito viene illustrata la struttura degli elementi che verranno utilizzati:


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



Tenendo presente la semplice struttura degli elementi, è possibile avere senso degli attributi che rendono univoco ogni elemento. I dettagli di ogni elemento verranno trattati negli argomenti rimanenti di questa sezione. Per ulteriori informazioni sugli elementi e sugli attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




