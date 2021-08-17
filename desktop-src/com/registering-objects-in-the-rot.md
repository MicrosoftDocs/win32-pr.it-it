---
title: Registrazione di oggetti nella ROT
description: Registrazione di oggetti nella ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77e7bc6fe8b0a4d5896bf33575df2f57fb0e583f78acd02653f6ccb014f34ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104814"
---
# <a name="registering-objects-in-the-rot"></a>Registrazione di oggetti nella ROT

In genere, quando un client chiede a un server di creare un'istanza dell'oggetto, il server crea in genere un moniker per l'oggetto e lo registra nella tabella degli oggetti in esecuzione (ROT) tramite una chiamata a [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Quando il server chiama [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) per creare un moniker di file da registrare nella rot, i server devono passare nomi di file locali basati su unità, non in formato UNC. Ciò garantisce che i dati di confronto del moniker generati dalla chiamata al registro ROT corrispondano a quanto usato durante una ricerca ROT da parte di un client remoto. Ciò è dovuto al fatto che quando il servizio COM distribuito riceve una richiesta di attivazione per un file locale al server da un client remoto, il file viene convertito in un percorso basato su unità locale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Installazione come applicazione di servizio](installing-as-a-service-application.md)
</dt> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 




