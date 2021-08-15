---
description: Un modello ha la definizione della sintassi seguente.
ms.assetid: 77eb739d-8da3-4481-8dd1-f9f2f0eda136
title: Modelli (formato di file X)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbae3f8c74dcf2905ee38e948b7c128b6fd79bd0c469bdba6dfd721095070e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523402"
---
# <a name="templates-x-file-format-binary-encoding"></a>Modelli (formato di file X, codifica binaria)

Un modello ha la definizione della sintassi seguente.


```
template              : TOKEN_TEMPLATE name TOKEN_OBRACE
                            class_id
                            template_parts
                            TOKEN_CBRACE

template_parts        : template_members_part TOKEN_OBRACKET
                        template_option_info
                        TOKEN_CBRACKET
                      | template_members_list

template_members_part : /* Empty */
                      | template_members_list

template_option_info  : ellipsis
                      | template_option_list

template_members_list :    template_members
                      | template_members_list template_members

template_members      : primitive
                      | array
                      | template_reference

primitive             : primitive_type optional_name TOKEN_SEMICOLON

array                 : TOKEN_ARRAY array_data_type name dimension_list
                        TOKEN_SEMICOLON

template_reference    : name optional_name YT_SEMICOLON

primitive_type        : TOKEN_WORD
                      | TOKEN_DWORD
                      | TOKEN_FLOAT
                      | TOKEN_DOUBLE
                      | TOKEN_CHAR
                      | TOKEN_UCHAR
                      | TOKEN_SWORD
                      | TOKEN_SDWORD
                      | TOKEN_LPSTR
                      | TOKEN_UNICODE
                      | TOKEN_CSTRING

array_data_type       : primitive_type
                      | name

dimension_list        : dimension
                      | dimension_list dimension

dimension             : TOKEN_OBRACKET dimension_size TOKEN_CBRACKET

dimension_size        : TOKEN_INTEGER
                      | name

template_option_list  : template_option_part
                      | template_option_list template_option_part

template_option_part  : name optional_class_id

name                  : TOKEN_NAME

optional_name         : /* Empty */
                      | name

class_id              : TOKEN_GUID

optional_class_id     : /* Empty */
                      | class_id

ellipsis              : TOKEN_DOT TOKEN_DOT TOKEN_DOT
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica binaria](binary-encoding.md)
</dt> </dl>

 

 



