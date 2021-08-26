---
title: Informazioni sui .NET Framework dati
description: Informazioni sui .NET Framework dati
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,.NET Framework
- Windows Media Player a oggetti, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Dispositivi mobili, .NET Framework
- Windows Media Player ActiveX controllo, .NET Framework
- Windows Media Player Controllo ActiveX per dispositivi mobili,.NET Framework
- ActiveX,.NET Framework
- .NET Framework,tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36854d971b0fc220f8f77b754b08b486ff93d339935bedcf33edca39fb701e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004520"
---
# <a name="about-net-framework-data-types"></a>Informazioni sui .NET Framework dati

Questa sezione contiene le informazioni necessarie per convertire le informazioni di riferimento sul modello a oggetti orientate agli script in tipi di dati .NET Framework di base di Microsoft. Il riferimento allo script Windows Media Player contiene quasi tutte le informazioni necessarie per usare il controllo Windows Media Player in un programma basato su .NET Framework e nella maggior parte dei casi, la sintassi sarà simile a quella di altri linguaggi di scripting, ad esempio Microsoft JScript.

Il Windows Media Player fornisce il tipo JScript dati e, se necessario, la conversione C++. Ad esempio, un **numero potrebbe** essere restituito da un metodo . JScript considera tutti i numeri nello stesso modo, ma altri linguaggi distinguono tra tipi diversi di numeri (integer, virgola mobile e così via). Il riferimento fornisce la conversione C++ per i tipi di dati number perché i numeri possono essere elaborati in modo diverso da C++. Ad esempio, C++ usa il **tipo di** dati int per l'aritmetica integer e **float** per la virgola mobile.

Il .NET Framework usa un sistema leggermente diverso di tipi di dati di base. Nella tabella seguente vengono illustrate le differenze nei tipi di dati comuni che è probabile utilizzare. Per altre informazioni sull'.NET Framework di dati di base e sulla conversione in altri sistemi di tipi di dati, vedere la discussione .NET Framework Developer's Guide (Guida per gli sviluppatori di .NET Framework) sui tipi di dati di base dello spazio dei nomi di sistema.

Questa tabella fornisce il nome .NET Framework classe e il tipo di dati C#. I tipi di dati per altri linguaggi vengono definiti per ogni linguaggio nei rispettivi riferimenti al linguaggio.



| Tipo di dati script | Tipo di dati C++     | .NET Framework classe (tipo di dati C#) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**double**)               |
| **Number**       | **float**         | **Single** (**float**)                |
| **Stringa**       | **BSTR**          | **String** (**string**)               |
| **Boolean**      | **VARIANT \_ BOOL** | **Boolean** (**bool**)                |
| **Object**       | **Object**        | **Object** **(oggetto**)               |



 

Se si usa Visual Studio, è possibile usare la tecnologia Microsoft IntelliSense per determinare il tipo di dati previsto per una funzione specifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Windows Media Player in una .NET Framework soluzione**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




