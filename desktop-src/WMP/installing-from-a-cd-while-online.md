---
title: Installazione da un CD in modalità online
description: Installazione da un CD in modalità online
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player online, installazione da CD mentre è online
- online store, installazione da CD mentre è online
- tipo 1 store online, installazione da CD mentre è online
- tipo 2 negozi online, installazione da CD mentre è online
- Windows Media Player store online, installazioni online da CD
- online store, installazioni online da CD
- store online di tipo 1, installazioni online da CD
- store online di tipo 2, installazioni online da CD
- Windows Media Player online, l'installazione di CD mentre è online
- negozi online, installazioni di CD mentre sono online
- type 1 online stores,CD installs while online
- store online di tipo 2, installazioni di CD durante l'installazione online
- installazione di negozi online da CD mentre è online
- Installazioni da CD di negozi online mentre sono online
- installazioni online di negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13589d7ba6dea0693acaacb5e0d1f551b4a4f178c4ccb50a1bd8ebb513dda3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996511"
---
# <a name="installing-from-a-cd-while-online"></a>Installazione da un CD in modalità online

Gli utenti possono Windows Media Player da un CD mentre sono connessi a Internet. In questo caso, Windows Media Player il programma di installazione individua il documento ServiceInfo specificato dal parametro della riga di comando *ServiceInfo.* Se **l'attributo Key** corrisponde al parametro della riga di comando *DefaultService,* il programma di installazione esamina l'elemento Install per personalizzare il processo di installazione. Usando i valori degli attributi, il programma di installazione visualizza il contratto di licenza con l'utente finale e l'informativa sulla privacy e recupera e installa il file .cab nel computer dell'utente. Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.

Dopo l'installazione, Windows Media Player lo store online iniziale usando il nome della chiave specificato per il parametro della riga di comando *DefaultService.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Impostazione dello Store online iniziale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




