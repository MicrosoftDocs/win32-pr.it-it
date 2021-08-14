---
title: Configurare i parametri della riga di comando per i negozi online
description: Configurare i parametri della riga di comando per i negozi online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player online, configurare i parametri della riga di comando
- online stores,setup command-line parameters
- tipo 1 punti vendita online, parametri della riga di comando di installazione
- type 2 online stores,setup command-line parameters
- parametri della riga di comando di installazione
- Windows Media Player online store,parametri della riga di comando
- online stores, parametri della riga di comando
- digitare 1 punti vendita online, parametri della riga di comando
- tipo 2 punti vendita online, parametri della riga di comando
- parametri da riga di comando
- Windows Media Player online store,parameters
- online stores,parameters
- tipo 1 punti vendita online, parametri
- tipo 2 punti vendita online, parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77df581b2be4b2539772065e1aabef281a4c6c931ca115a4f6331063cf2414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569302"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Configurare i parametri della riga di comando per i negozi online

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Quando si installa Windows Media Player 10 o Windows Media Player 11 in Windows XP, è possibile aggiungere parametri della riga di comando per specificare il primo negozio online visualizzato dall'utente.

Sintassi


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parametri

DefaultService (obbligatorio)

Nome della chiave per lo store online. Questo valore deve corrispondere al nome della chiave **nell'attributo Key** dell'elemento **ServiceInfo** del documento ServiceInfo.

ServiceInfo (obbligatorio)

Percorso completo di un documento ServiceInfo installato nel computer dell'utente.

ServiceExtra (facoltativo)

Una stringa di query Windows Media Player 10 verrà aggiunta all'URL per il documento ServiceInfo quando recupera il documento online.

## <a name="remarks"></a>Commenti

Per informazioni dettagliate sulla ridistribuzione Windows Media Player software con l'applicazione, vedere [Ridistribuzione Windows Media Player Software.](redistributing-windows-media-player-software.md)

Quando il computer dell'utente non è connesso a Internet, le informazioni contenute nel documento ServiceInfo locale vengono usate per configurare Windows Media Player per il servizio attivo iniziale.

Per i parametri della riga di comando viene fatto distinzione tra maiuscole e minuscole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Co-personalizzazione di negozi online**](co-branding-online-stores.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Impostazione dello Store online iniziale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




