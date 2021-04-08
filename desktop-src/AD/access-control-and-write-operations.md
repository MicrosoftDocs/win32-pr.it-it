---
title: Operazioni di scrittura e controllo di accesso
description: Le modifiche alle proprietà hanno esito negativo se il chiamante non dispone di diritti sufficienti.
ms.assetid: eb5b97fb-4654-444e-9f5a-9a4be27ef1a3
ms.tgt_platform: multiple
keywords:
- AD Access Control e writer Operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b8ecab475cd5696a98c985f92ccc24b1dd6072
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872238"
---
# <a name="access-control-and-write-operations"></a>Operazioni di scrittura e controllo di accesso

Le modifiche alle proprietà hanno esito negativo se il chiamante non dispone di diritti sufficienti. Per le operazioni di scrittura che comportano la modifica in batch di più proprietà, l'intera operazione ha esito negativo se il chiamante non dispone dei diritti necessari per una sola delle proprietà modificate. È ad esempio possibile eseguire più chiamate [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare più proprietà in un oggetto. Tuttavia, quando si chiama [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per scrivere i nuovi dati dalla cache locale alla directory, le **informazioni** non riusciranno se il chiamante non dispone dell'accesso in scrittura a tutte le proprietà modificate. Analogamente, il metodo [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) non è in grado di impostare alcuna proprietà se il chiamante non ha accesso a tutte le proprietà impostate. Pertanto, è necessario raggruppare più operazioni di modifica solo se si è certi che tutte le modifiche verranno eseguite correttamente. Per determinare gli attributi di un oggetto directory che il chiamante è in grado di modificare, leggere l'attributo **allowedAttributesEffective** dell'oggetto.

Se il chiamante non dispone di diritti sufficienti per modificare una proprietà, è possibile che vengano restituiti i seguenti codici restituiti:

proprietà \_ e \_ Ads \_ non \_ impostati e \_ \_ Proprietà Ads \_ non \_ modificata

 

 