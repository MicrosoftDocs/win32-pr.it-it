---
description: Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e i moduli unione usando gli analizzatori di coerenza interna - ICO.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Uso di Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527124"
---
# <a name="using-evalcom2"></a>Uso di Evalcom2

Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e i moduli unione usando gli analizzatori di coerenza [interna - ICE.](internal-consistency-evaluators-ices.md) L'oggetto principale implementa le interfacce per i programmi C/C++.

L'oggetto principale implementa anche [le interfacce Evalcom2 per](evalcom2-interfaces.md) i programmi C/C++. Il CLSID necessario per ottenere l'interfaccia da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) è {6E5E1910-8053-4660-B795-6B612E29BC58}. REFIID è {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

È possibile utilizzare la procedura seguente per implementare le operazioni di convalida.

**Per implementare le operazioni di convalida**

1.  Inizializzare COM nel thread chiamante usando [**CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize)
2.  Ottenere il puntatore [**all'interfaccia IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) usando [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
3.  Aprire il pacchetto di installazione o il modulo unione usando il [**metodo OpenDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase)
4.  Aprire il file di valutazione usando [**il metodo OpenCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub)
5.  Impostare la funzione di callback di visualizzazione usando [**il metodo SetDisplay.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay)
6.  Impostare la funzione di callback dello stato usando [**il metodo SetStatus.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus)
7.  Eseguire la convalida usando il [**metodo Validate.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate)
8.  Chiudere il file con estensione cub usando [**il metodo CloseCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub)
9.  Chiudere il database usando il [**metodo CloseDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase)
10. Rilasciare [**l'interfaccia IValidate.**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate)
11. Annullare l'inizializzazione COM [**tramite CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce Evalcom2](evalcom2-interfaces.md)
</dt> <dt>

[Automazione della convalida](validation-automation.md)
</dt> <dt>

[Funzioni di callback di convalida](validation-callback-functions.md)
</dt> </dl>

 

 
