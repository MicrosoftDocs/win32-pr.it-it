---
title: Configurare i parametri della riga di comando per i negozi online
description: Configurare i parametri della riga di comando per i negozi online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Online Stores, configurare i parametri della riga di comando
- negozi online, parametri della riga di comando di installazione
- digitare 1 archivi online, impostare i parametri della riga di comando
- digitare 2 archivi online, impostare i parametri della riga di comando
- Imposta parametri della riga di comando
- Windows Media Player Online Store, parametri della riga di comando
- archivi online, parametri della riga di comando
- digitare 1 archivi online, parametri della riga di comando
- digitare 2 archivi online, parametri della riga di comando
- parametri da riga di comando
- Windows Media Player Online Stores, parametri
- negozi online, parametri
- digitare 1 archivi online, parametri
- digitare 2 archivi online, parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044647"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Configurare i parametri della riga di comando per i negozi online

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Quando si installa Windows Media Player 10 o Windows Media Player 11 in Windows XP, è possibile aggiungere i parametri della riga di comando per specificare il primo negozio online visualizzato dall'utente.

Sintassi


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parametri

DefaultService (obbligatorio)

Nome della chiave per l'archivio online. Questo valore deve corrispondere al nome della chiave nell'attributo **chiave** dell'elemento **ServiceInfo** del documento ServiceInfo.

ServiceInfo (obbligatorio)

Percorso completo di un documento ServiceInfo installato nel computer dell'utente.

ServiceExtra (facoltativo)

Stringa di query che verrà aggiunta da Windows Media Player 10 all'URL del documento ServiceInfo quando il documento viene recuperato in linea.

## <a name="remarks"></a>Commenti

Per informazioni dettagliate sulla ridistribuzione del software Windows Media Player con l'applicazione, vedere [ridistribuzione del software windows media player](redistributing-windows-media-player-software.md).

Quando il computer dell'utente non è connesso a Internet, le informazioni contenute nel documento ServiceInfo locale vengono usate per configurare Windows Media Player per il servizio attivo iniziale.

I parametri della riga di comando fanno distinzione tra maiuscole e minuscole

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Negozi online di co-branding**](co-branding-online-stores.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Impostazione dell'archivio online iniziale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




