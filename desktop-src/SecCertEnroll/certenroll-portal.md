---
description: Esempio di certificato. Creare applicazioni per la certificazione API, installare il certificato SSL, il certificato del server, creare un certificato su supporti, ad esempio Internet o una intranet, che non sono intrinsecamente sicuri.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API di registrazione certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df9caf38f22ac2c8ca8b13e6ca471eea94ae10b5c01ee2da7b4c2247844a70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902961"
---
# <a name="certificate-enrollment-api"></a>API di registrazione certificato

## <a name="purpose"></a>Scopo

L'API di registrazione certificati può essere usata per creare un'applicazione client per richiedere un certificato e installare una risposta del certificato. Questa API viene implementata in CertEnroll.dll a partire da Windows Vista; sostituisce Xenroll.dll.

## <a name="developer-audience"></a>Sviluppatori

L'API di registrazione certificati può essere utilizzata dagli sviluppatori di applicazioni che consentiranno agli utenti di creare, richiedere e recuperare certificati su supporti, ad esempio Internet o Intranet, che non sono intrinsecamente sicuri. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++, il Component Object Model (COM) e l'Windows di programmazione basato su Windows. Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia e l'infrastruttura a chiave pubblica.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API di registrazione certificati è supportata a partire da Windows Server 2008 e Windows Vista. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sull'API di registrazione certificati](about-the-certificate-enrollment-api.md)<br/> | Vengono illustrati i concetti chiave relativi alle richieste di certificati.<br/>                                                                                                      |
| [Uso dell'API di registrazione certificati](using-the-certificate-enrollment-api.md)<br/> | Come usare l'API di registrazione certificati per estendere le funzionalità di Servizi certificati Active Directory.<br/>                                              |
| [Informazioni di riferimento sulle API di registrazione certificati](certificate-enrollment-api-reference.md)<br/> | Descrizioni dettagliate di interfacce, enumerazioni e altri elementi di programmazione che possono essere utilizzati per registrare un utente o un computer in una gerarchia di certificati.<br/> |



 

 

 




