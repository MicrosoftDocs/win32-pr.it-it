---
description: Accesso a un valore del Registro di sistema senza nome
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Accesso a un valore del Registro di sistema senza nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62a82cfdb9d90ba11a177891ad7ee5e3310207825bd9a155c5eda3b10c4e68e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131924"
---
# <a name="accessing-an-unnamed-registry-value"></a>Accesso a un valore del Registro di sistema senza nome

Il valore predefinito o senza nome di una chiave del Registro di sistema viene visualizzato come (predefinito) o <No Name> nell'editor del Registro di sistema Regedit. È possibile usare il provider del Registro di sistema per accedere a una chiave del Registro di sistema senza nome. Analogamente, è anche possibile usare il provider del Registro di sistema per accedere alle descrizioni delle bitmap, definite come valori senza nome.

La procedura seguente descrive come recuperare un valore del Registro di sistema senza nome.

**Per recuperare un valore del Registro di sistema senza nome**

1.  Definire una proprietà e impostare il **qualificatore PropertyContext** di tale proprietà su una stringa vuota.

    Nell'esempio di codice seguente viene illustrato come la classe definisce le proprietà per contenere i valori per la chiave specificata dal **qualificatore ClassContext.** Il valore predefinito viene archiviato nella **proprietà** Default.

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    La chiave Transports non usa il valore senza nome, quindi la compilazione di questo file MOF non produce alcun valore per la proprietà **Default** a meno che non venga usato uno strumento di modifica del Registro di sistema per modificare il valore senza nome.

2.  Per un file bitmap, definire una proprietà e impostare **l'oggetto PropertyContext** di tale proprietà.

    Nell'esempio di codice seguente viene illustrato come definire una proprietà .

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



