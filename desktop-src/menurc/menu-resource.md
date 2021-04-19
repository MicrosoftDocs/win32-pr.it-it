---
title: Risorsa MENU
description: Definisce il contenuto di una risorsa di menu. | Risorsa MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- MENU delle risorse di MENU e altre risorse
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321896"
---
# <a name="menu-resource"></a>Risorsa MENU

Definisce il contenuto di una risorsa di menu. Una risorsa di menu è una raccolta di informazioni che definiscono l'aspetto e la funzione di un menu dell'applicazione. Un menu è uno strumento di input speciale che consente a un utente di selezionare i comandi e aprire sottomenu da un elenco di voci di menu.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*
</dt> <dd>

Numero che identifica il menu. Questo valore è una stringa univoca o un valore Unsigned Integer univoco a 16 bit nell'intervallo compreso tra 1 e 65.535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Questo parametro può essere costituito da zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caratteristiche**](characteristics-statement.md) *DWORD*     | Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse. Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md). |
| [](language-statement.md) *Lingua* lingua, *lingua* | Lingua per la risorsa. Per ulteriori informazioni, vedere [**Language**](language-statement.md).                                                                                            |
| [](version-statement.md) *DWORD* versione                     | Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse. Per ulteriori informazioni, vedere [**Version**](version-statement.md).              |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di un'istruzione di **menu** completa:

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di menu](./using-menus.md)
</dt> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 
