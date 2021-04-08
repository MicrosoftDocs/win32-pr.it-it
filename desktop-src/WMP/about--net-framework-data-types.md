---
title: Informazioni sui tipi di dati .NET Framework
description: Informazioni sui tipi di dati .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player, .NET Framework
- Modello a oggetti Media Player Windows, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Windows Media Player ActiveX Control, .NET Framework
- Controllo ActiveX Windows Media Player Mobile, .NET Framework
- Controllo ActiveX, .NET Framework
- .NET Framework, tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045214"
---
# <a name="about-net-framework-data-types"></a>Informazioni sui tipi di dati .NET Framework

Questa sezione contiene le informazioni necessarie per tradurre il riferimento del modello a oggetti orientato allo script in Microsoft .NET tipi di dati di base del Framework. Il riferimento agli script di Windows Media Player include quasi tutte le informazioni necessarie per utilizzare il controllo Media Player di Windows in un programma basato su .NET Framework e, nella maggior parte dei casi, la sintassi sarà simile a quella di altri linguaggi di scripting, ad esempio Microsoft JScript.

Il riferimento a Windows Media Player fornisce il tipo di dati JScript e, se necessario, la conversione in C++. Un **numero** , ad esempio, potrebbe essere restituito da un metodo. JScript considera tutti i numeri nello stesso modo, ma altri linguaggi distinguono tra tipi diversi di numeri (Integer, virgola mobile e così via). Il riferimento fornisce la conversione C++ per i tipi di dati numerici perché i numeri possono essere elaborati in modo diverso in C++. Ad esempio, C++ usa il tipo di dati **int** per i calcoli Integer e **float** per virgola mobile.

Il .NET Framework utilizza un sistema leggermente diverso di tipi di dati di base. Nella tabella seguente vengono illustrate le differenze nei tipi di dati comuni che è probabile utilizzare. Per ulteriori informazioni su .NET Framework tipi di dati di base e sulla conversione ad altri sistemi con tipi di dati, vedere la guida per gli sviluppatori .NET Framework informazioni sui tipi di dati di base dello spazio dei nomi del sistema.

Questa tabella indica il nome della classe .NET Framework e il tipo di dati C#. I tipi di dati per le altre lingue vengono definiti per ogni lingua nei rispettivi riferimenti al linguaggio.



| Tipo di dati script | Tipo di dati C++     | Classe .NET Framework (tipo di dati C#) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**Double**)               |
| **Number**       | **float**         | **Singolo** (**float**)                |
| **Stringa**       | **BSTR**          | **String** (**stringa**)               |
| **Boolean**      | **\_bool Variant** | **Boolean** (**bool**)                |
| **Object**       | **Object**        | **Oggetto** (**oggetto**)               |



 

Se si utilizza Visual Studio, è possibile utilizzare la tecnologia Microsoft IntelliSense per determinare il tipo di dati previsto per una funzione specifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Incorporamento del controllo Media Player Windows in una soluzione .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




