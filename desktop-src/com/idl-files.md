---
title: File IDL
description: File IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873009"
---
# <a name="idl-files"></a>File IDL

COM usa il Microsoft Interface Definition Language (MIDL) per descrivere gli oggetti COM. MIDL è un'estensione dell'IDL per gli ambienti di calcolo distribuiti definiti da Open Software Foundation, sviluppato per definire interfacce per le chiamate di procedure remote in applicazioni client/server tradizionali. MIDL include la maggior parte degli attributi e delle istruzioni del linguaggio di definizione dell'oggetto (FAD), il linguaggio originariamente usato per generare librerie dei tipi per l'automazione OLE.

In C++ e Java uno sviluppatore che compila un oggetto COM crea un file IDL che viene elaborato dal compilatore MIDL per creare una libreria dei tipi, un file di intestazione e proxy o entrambi. Una *libreria dei tipi* è un file binario che descrive l'oggetto com o le interfacce com oppure entrambe. Una libreria dei tipi è la versione compilata del file IDL. Tuttavia, le librerie di tipi supportano solo la semantica di FAD. In particolare, non possono rappresentare tutte le informazioni provenienti da un file IDL correlato agli attributi IDL, ad esempio le \[ [**dimensioni \_**](/windows/desktop/Midl/size-is) \] . È necessario creare e utilizzare i file proxy per i file IDL interessati dalla perdita di informazioni nella libreria dei tipi.

In Visual Basic, uno sviluppatore che crea un oggetto COM non crea un file IDL. Al contrario, Visual Basic raccoglie le informazioni usando le proprietà di classe e progetto e crea direttamente la libreria dei tipi.

 

 