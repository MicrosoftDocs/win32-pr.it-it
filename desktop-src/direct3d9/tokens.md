---
description: I token vengono scritti come parole little-endian. Il seguente elenco di valori di token è suddiviso in token di registrazione e autonomi.
ms.assetid: vs|directx_sdk|~\tokens.htm
title: Tokens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df253327b1256ea5e04f8b80b7e1da89f13e32c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304366"
---
# <a name="tokens"></a><span data-ttu-id="d8b43-104">Tokens</span><span class="sxs-lookup"><span data-stu-id="d8b43-104">Tokens</span></span>

<span data-ttu-id="d8b43-105">I token vengono scritti come parole little-endian.</span><span class="sxs-lookup"><span data-stu-id="d8b43-105">Tokens are written as little-endian WORDs.</span></span> <span data-ttu-id="d8b43-106">Il seguente elenco di valori di token è suddiviso in token di registrazione e autonomi.</span><span class="sxs-lookup"><span data-stu-id="d8b43-106">The following list of token values is divided into record-bearing and stand-alone tokens.</span></span>

<span data-ttu-id="d8b43-107">I token che portano a record sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="d8b43-107">The record-bearing tokens are defined as follows.</span></span>


```
#define TOKEN_NAME         1
#define TOKEN_STRING       2
#define TOKEN_INTEGER      3
#define TOKEN_GUID         5
#define TOKEN_INTEGER_LIST 6
#define TOKEN_FLOAT_LIST   7
```



<span data-ttu-id="d8b43-108">I token autonomi sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="d8b43-108">The stand-alone tokens are defined as follows.</span></span>


```
#define TOKEN_OBRACE      10
#define TOKEN_CBRACE      11
#define TOKEN_OPAREN      12
#define TOKEN_CPAREN      13
#define TOKEN_OBRACKET    14
#define TOKEN_CBRACKET    15
#define TOKEN_OANGLE      16
#define TOKEN_CANGLE      17
#define TOKEN_DOT         18
#define TOKEN_COMMA       19
#define TOKEN_SEMICOLON   20
#define TOKEN_TEMPLATE    31
#define TOKEN_WORD        40
#define TOKEN_DWORD       41
#define TOKEN_FLOAT       42
#define TOKEN_DOUBLE      43
#define TOKEN_CHAR        44
#define TOKEN_UCHAR       45
#define TOKEN_SWORD       46
#define TOKEN_SDWORD      47
#define TOKEN_VOID        48
#define TOKEN_LPSTR       49
#define TOKEN_UNICODE     50
#define TOKEN_CSTRING     51
#define TOKEN_ARRAY       52
```



## <a name="related-topics"></a><span data-ttu-id="d8b43-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8b43-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b43-110">Codifica binaria</span><span class="sxs-lookup"><span data-stu-id="d8b43-110">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



