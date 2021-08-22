---
description: L'applicazione deve creare le proprietà con un tipo di dati che esegue il mapping al tipo di dati del Registro di sistema.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mapping di un tipo di dati del Registro di sistema a un tipo di dati WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050689"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mapping di un tipo di dati del Registro di sistema a un tipo di dati WMI

L'applicazione deve creare le proprietà con un tipo di dati che esegue il mapping al tipo di dati del Registro di sistema. Non è necessario specificare il tipo di dati del Registro di sistema nei metodi che creano, ottengono o impostano i valori del Registro di sistema. Tuttavia, il parametro di input che contiene il valore deve essere nel tipo di dati WMI corretto. Ad esempio, se un'applicazione riceve dati **\_ DWORD REG** dal Registro di sistema, la classe che riceve i dati deve includere una **proprietà Uint32.**

La tabella seguente elenca il mapping tra i tipi di dati del Registro di sistema e WMI usati nei [**metodi StdRegProv.**](/previous-versions/windows/desktop/regprov/stdregprov)



| Tipo di dati del Registro di sistema      | Tipo di dati WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ BINARY**         | **Matrice uint8**<br/> Matrice di valori che non superano 255 o FF esadecimali. Ad esempio, il codice script Visual Basic seguente crea una matrice adatta a questo tipo di dati.<br/> `BinArray = Array(&H01, &Ha2)`<br/> Il [**metodo della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) richiede il tipo di dati **REG \_ BINARY.**<br/>                                                                                          |
| **REG \_ DWORD**          | **uint32,** **sint32** o Visual Basic **integer**<br/> Singolo valore a 32 bit. I [**metodi della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) e [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) richiedono il tipo di dati **REG \_ DWORD.**<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> Il [**metodo della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) richiede il tipo di dati **REG \_ SZ.**<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **uint64**.<br/> Singolo valore a 64 bit. I [**metodi della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) e [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) richiedono il tipo di dati **REG \_ QWORD.**<br/>                                                                                                                                                                                                         |
| **REG \_ EXPAND \_ SZ**     | **string**<br/> Le stringhe espanse sono stringhe speciali che rappresentano le variabili di ambiente di sistema. Ad esempio, il codice VBScript seguente crea una stringa che rappresenta la **variabile di ambiente HKEY LOCAL \_ \_ USER** TEMP.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> Il [**metodo della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) richiede il tipo di dati **REG EXPAND \_ \_ SZ.**<br/> |
| **REG \_ MULTI \_ SZ**      | **matrice di** stringhe<br/> Il tipo di dati Multistring contiene più stringhe. Ad esempio, il codice VBScript seguente crea una matrice adatta a questo tipo di dati.<br/> `MultiValue = Array("first", "second", "third")`<br/> Il [**metodo della classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) richiede il tipo di **dati REG MULTI \_ \_ SZ.**<br/>                                                                     |
| **ELENCO \_ DI RISORSE \_ REG** | A seconda dei casi. Per altre informazioni, vedere [Descrizione di una risorsa per il Registro di sistema.](describing-a-resource-for-the-registry.md)<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizione di classi per il provider del Registro di sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

