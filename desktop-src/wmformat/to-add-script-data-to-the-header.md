---
title: Per aggiungere dati di script all'intestazione
description: Per aggiungere dati di script all'intestazione
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, aggiunta di dati di script alle intestazioni
- Advanced Systems Format (ASF), aggiunta di dati di script alle intestazioni
- ASF (Advanced Systems Format), aggiunta di dati di script alle intestazioni
- script, aggiunta di dati alle intestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a8ad34a69427dc26435a6a599b8d91db2ebe2b8be700483189b2e7ba22846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027319"
---
# <a name="to-add-script-data-to-the-header"></a>Per aggiungere dati di script all'intestazione

È possibile includere comandi script nell'intestazione di un file ASF. Per scrivere comandi script nell'intestazione al momento della codifica, seguire questa procedura. Eseguire questi passaggi prima di chiamare [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

1.  Ottenere un puntatore **all'interfaccia IWMHeaderInfo** chiamando **IWMWriter::QueryInterface.**
2.  Aggiungere ogni comando di script desiderato chiamando [**IWMHeaderInfo::AddScript.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript) Ogni chiamata accetta le due stringhe separatamente e l'ora di presentazione da usare per il comando come parametri.

Quando un'applicazione legge il file, dovrà recuperare tutti i comandi script. Per trovare tutti i comandi script nell'intestazione di un file, seguire questa procedura. Questa operazione deve essere eseguita prima di avviare la riproduzione.

1.  Ottenere un puntatore **all'interfaccia IWMHeaderInfo** dell'oggetto reader (o oggetto lettore sincrono) chiamando il **metodo QueryInterface** di un'altra interfaccia nell'oggetto.
2.  Ottenere il numero totale di script nell'intestazione chiamando [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Scorrere tutti gli script nell'intestazione uno alla volta usando le chiamate a [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Creare un elenco degli orari di presentazione in modo che l'applicazione possa reagire ai comandi al momento appropriato.

> [!Note]  
> Quando si usa DRM per crittografare un file, nessun comando script può avere un'ora di presentazione di 0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




