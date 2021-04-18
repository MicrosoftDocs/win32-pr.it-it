---
title: Installazione da un CD mentre è in linea
description: Installazione da un CD mentre è in linea
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online Stores, installazione da CD mentre è online
- negozi online, installazione da CD mentre è online
- digitare 1 negozi online, installazione da CD mentre è in linea
- digitare 2 archivi online, installazione da CD mentre è in linea
- Windows Media Player Online Stores, installazioni online da CD
- negozi online, installazioni online da CD
- digitare 1 negozi online, installazioni online da CD
- digitare 2 archivi online, installazioni online da CD
- Windows Media Player Online Stores, installazione CD in linea
- negozi online, installazioni CD in linea
- digitare 1 negozi online, installazione CD mentre è in linea
- digitare 2 negozi online, installazioni CD mentre è online
- installazione di archivi online da CD in linea
- Installazioni CD di negozi online in linea
- installazioni online di archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298430"
---
# <a name="installing-from-a-cd-while-online"></a>Installazione da un CD mentre è in linea

Gli utenti possono installare Windows Media Player da un CD mentre si è connessi a Internet. In questo caso, il programma di installazione di Windows Media Player individua il documento ServiceInfo specificato dal parametro della riga di comando *ServiceInfo* . Se l'attributo **chiave** corrisponde al parametro della riga di comando *DefaultService* , il programma di installazione controlla l'elemento install per personalizzare il processo di installazione. Utilizzando i valori di attributo, il programma di installazione Visualizza il contratto di licenza con l'utente finale (EULA) e l'informativa sulla privacy, nonché recupera e installa il file CAB nel computer dell'utente. Ad esempio, è possibile usare questa funzionalità per installare la versione più recente di un oggetto COM richiesto dal negozio online.

Una volta installato, Windows Media Player imposta l'archivio online iniziale usando il nome della chiave specificato per il parametro della riga di comando *DefaultService* .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Impostazione dell'archivio online iniziale**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




