---
title: Uso di nuovi tipi di dati nel file IDL
description: Il file di intestazione Basetsd.h definisce i nuovi tipi di dati necessari per la scrittura di applicazioni eseguite in applicazioni a 32 e a 64 bit Windows.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- File di intestazione Basetsd.h a 64 bit Windows programmazione
- tipi di dati nel file IDL a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccb29ee654dc2ecc1459a4a3e8ba549e8f78a8af26a305725dbce90f469881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993921"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Uso di nuovi tipi di dati nel file IDL

Il file di intestazione Basetsd.h definisce i nuovi tipi di dati necessari per la scrittura di applicazioni eseguite in applicazioni a 32 e a 64 bit Windows. Per usare questi tipi di dati nelle interfacce, importare Basetsd.h nel file IDL. Non includere \# il file o si avranno più definizioni in fase di compilazione.

In alternativa, è possibile includere o importare il file Basetsd.idl nel file IDL.

Per altre informazioni sull'aggiunta di file di intestazione di sistema al file IDL, vedere [Importazione](/windows/desktop/Midl/importing-files-and-type-libraries) di file e librerie dei tipi e [Importazione di file di intestazione di sistema.](/windows/desktop/Midl/importing-system-header-files)

 

 