---
description: Un oggetto dati presenta la seguente definizione di sintassi.
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: Data (formato file X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123366"
---
# <a name="data-x-file-format-binary-encoding"></a>Data (formato file X, codifica binaria)

Un oggetto dati presenta la seguente definizione di sintassi.


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



Si noti che nei \_ file binari nell'elenco di numeri e nei \_ dati di elenco float \_ \_ non vengono usati i punti e virgola del token. La virgola e il punto e virgola vengono usati nei dati dell'elenco di stringhe \_ . Si noti inoltre che è possibile utilizzare solo il \_ riferimento ai dati per i membri dati facoltativi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica binaria](binary-encoding.md)
</dt> </dl>

 

 



