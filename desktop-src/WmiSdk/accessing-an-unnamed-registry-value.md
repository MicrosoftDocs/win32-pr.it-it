---
description: Accesso a un valore del registro di sistema senza nome
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Accesso a un valore del registro di sistema senza nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317573"
---
# <a name="accessing-an-unnamed-registry-value"></a>Accesso a un valore del registro di sistema senza nome

Il valore predefinito o senza nome di una chiave del registro di sistema viene visualizzato come (impostazione predefinita) o <No Name> nell'editor del registro di sistema Regedit. Per accedere a una chiave del registro di sistema senza nome, è possibile utilizzare il provider del registro di sistema. Analogamente, è anche possibile usare il provider del registro di sistema per accedere alle descrizioni bitmap, definite come valori senza nome.

Nella procedura riportata di seguito viene descritto come recuperare un valore del registro di sistema senza nome.

**Per recuperare un valore del registro di sistema senza nome**

1.  Definire una proprietà e impostare il qualificatore **PropertyContext** della proprietà su una stringa vuota.

    Nell'esempio di codice seguente viene illustrato come la classe definisce le proprietà per mantenere i valori per la chiave specificata dal qualificatore **ClassContext** . Il valore predefinito viene archiviato nella proprietà **predefinita** .

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

    La chiave Transports non utilizza il valore senza nome, pertanto la compilazione di questo file MOF non produce alcun valore per la proprietà **predefinita** , a meno che non venga utilizzato uno strumento di modifica del registro di sistema per modificare il valore senza nome.

2.  Per un file bitmap, definire una proprietà e impostare il **PropertyContext** della proprietà.

    Nell'esempio di codice riportato di seguito viene illustrato come definire una proprietà.

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



