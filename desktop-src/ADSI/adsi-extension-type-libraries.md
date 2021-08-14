---
title: Librerie dei tipi dell'estensione ADSI
description: Le librerie dei tipi per le estensioni non vengono unite.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Librerie dei tipi dell'estensione ADSI ADSI
- estensioni ADSI, librerie dei tipi di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180831"
---
# <a name="adsi-extension-type-libraries"></a>Librerie dei tipi dell'estensione ADSI

Le librerie dei tipi per le estensioni non vengono unite. I client ADSI devono includere in modo specifico la libreria dei tipi per ogni estensione. La libreria dei tipi è necessaria per consentire Visual Basic le associazioni anticipate. Le applicazioni client scritte in C/C++ possono chiamare il **metodo QueryInterface** sulle interfacce di estensione definite nei file di intestazione dell'estensione.

 

 




