---
title: File IDL
description: File IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e2329d14ea844658bf9ad08927ddcef5067debed7a1c8a424c06d3c7adb8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992901"
---
# <a name="idl-files"></a>File IDL

COM usa il Microsoft Interface Definition Language (MIDL) per descrivere gli oggetti COM. MIDL è un'estensione del linguaggio IDL per gli ambienti di elaborazione distribuita definita da Open Software Foundation, sviluppata per definire le interfacce per le chiamate di procedura remota nelle applicazioni client/server tradizionali. MIDL include la maggior parte degli attributi e delle istruzioni di Object Definition Language (ODL), il linguaggio usato originariamente per generare librerie dei tipi per l'automazione OLE.

In C++ e Java uno sviluppatore che compila un oggetto COM crea un file IDL che il compilatore MIDL elabora quindi per creare una libreria dei tipi o file di intestazione e proxy o entrambi. Una *libreria dei* tipi è un file binario che descrive l'oggetto COM, le interfacce COM o entrambe. Una libreria dei tipi è la versione compilata del file IDL. Tuttavia, le librerie dei tipi supportano solo la semantica ODL. In particolare, non possono rappresentare tutte le informazioni da un file IDL correlato agli attributi IDL, ad esempio \[ [**size \_ è**](/windows/desktop/Midl/size-is) \] . È necessario creare e usare file proxy per i file IDL interessati dalla perdita di informazioni nella libreria dei tipi.

In Visual Basic uno sviluppatore che crea un oggetto COM non crea un file IDL. Al contrario, Visual Basic le informazioni usando le proprietà della classe e del progetto e crea direttamente la libreria dei tipi.

 

 