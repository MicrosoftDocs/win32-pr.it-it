---
title: Librerie di tipi di estensione ADSI
description: Le librerie dei tipi per le estensioni non sono unite.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI (librerie di tipi di estensione ADSI)
- estensioni ADSI, librerie di tipi di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515478"
---
# <a name="adsi-extension-type-libraries"></a>Librerie di tipi di estensione ADSI

Le librerie dei tipi per le estensioni non sono unite. I client ADSI devono includere specificamente la libreria dei tipi per ogni estensione. La libreria dei tipi è necessaria per Visual Basic per abilitare le associazioni iniziali. Le applicazioni client scritte in C/C++ possono chiamare il metodo **QueryInterface** sulle interfacce di estensione definite nei file di intestazione dell'estensione.

 

 




