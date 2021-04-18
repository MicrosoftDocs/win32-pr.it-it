---
description: L'applicazione deve creare le proprietà con un tipo di dati che esegue il mapping al tipo di dati del registro di sistema.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mapping di un tipo di dati del registro di sistema a un tipo di dati WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b96a3bcda0060e376427375059f006e3241118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529761"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mapping di un tipo di dati del registro di sistema a un tipo di dati WMI

L'applicazione deve creare le proprietà con un tipo di dati che esegue il mapping al tipo di dati del registro di sistema. Non è necessario specificare il tipo di dati del registro di sistema nei metodi che creano, ottengono o impostano valori del registro di sistema. Tuttavia, il parametro di input che contiene il valore deve essere nel tipo di dati WMI corretto. Se, ad esempio, un'applicazione riceve dati **reg \_ DWORD** dal registro di sistema, la classe che riceve i dati deve includere una proprietà **UInt32** .

Nella tabella seguente viene elencato il mapping tra il registro di sistema e i tipi di dati WMI utilizzati nei metodi [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) .



| Tipo di dati del registro di sistema      | Tipo di dati WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ binario**         | matrice **Uint8**<br/> Matrice di valori che non superano 255 o Hex FF. Il codice di script seguente Visual Basic crea ad esempio una matrice che corrisponde a questo tipo di dati.<br/> `BinArray = Array(&H01, &Ha2)`<br/> Il metodo della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) richiede il tipo di dati **\_ Binary reg** .<br/>                                                                                          |
| **REG \_ DWORD**          | **UInt32**, **sint32** o Visual Basic **Integer**<br/> Singolo valore a 32 bit. I metodi della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) e [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) richiedono il tipo di dati **reg \_ DWORD** .<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> Il metodo della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) richiede il tipo di dati **reg \_ SZ** .<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **UInt64**.<br/> Singolo valore a 64 bit. I metodi della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) e [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) richiedono il tipo di dati **reg \_ QWORD** .<br/>                                                                                                                                                                                                         |
| **REG \_ Espandi \_ SZ**     | **string**<br/> Le stringhe espanse sono stringhe speciali che rappresentano le variabili di ambiente di sistema. Ad esempio, il codice VBScript seguente crea una stringa che rappresenta la variabile di ambiente **\_ \_ utente locale HKEY** Temp.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> Il metodo della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) richiede il tipo di dati **reg \_ expand \_ SZ** .<br/> |
| **REG \_ - \_ SZ**      | matrice di **stringhe**<br/> Il tipo di dati multistringa contiene più stringhe. Il codice VBScript seguente, ad esempio, crea una matrice che corrisponde a questo tipo di dati.<br/> `MultiValue = Array("first", "second", "third")`<br/> Il metodo della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) richiede il tipo di dati **reg \_ \_ multisz** .<br/>                                                                     |
| **\_elenco delle risorse reg \_** | A seconda dei casi. Per ulteriori informazioni, vedere [Descrizione di una risorsa per il registro di sistema](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizione delle classi per il provider del registro di sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

