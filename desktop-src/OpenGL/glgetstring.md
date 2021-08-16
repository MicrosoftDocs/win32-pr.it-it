---
title: Funzione glGetString (Gl.h)
description: La funzione glGetString restituisce una stringa che descrive la connessione OpenGL corrente.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- Funzione glGetString OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cbc5a1add320d711c92020074b3de810d134e88953a8413c0efd2e6b6fdd954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359910"
---
# <a name="glgetstring-function"></a>Funzione glGetString

La **funzione glGetString** restituisce una stringa che descrive la connessione OpenGL corrente.

## <a name="syntax"></a>Sintassi


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Una delle costanti simboliche seguenti.



| Valore                                                                                                                                                         | Significato                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**FORNITORE DI \_ CONTABILITÀ GENERALE**</dt> </dl>             | Restituisce la società responsabile di questa implementazione OpenGL. Questo nome non cambia da versione a versione.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**GL \_ RENDERER**</dt> </dl>       | Restituisce il nome del renderer. Questo nome è in genere specifico di una particolare configurazione di una piattaforma hardware. Non cambia da versione a versione.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**VERSIONE DI GL \_**</dt> </dl>          | Restituisce un numero di versione o di versione.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**ESTENSIONI \_ GL**</dt> </dl> | Restituisce un elenco delimitato da spazi di estensioni supportate per OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *name* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetString** restituisce un puntatore a una stringa statica che descrive alcuni aspetti della connessione OpenGL corrente.

Poiché OpenGL non include query per le caratteristiche delle prestazioni di un'implementazione, è previsto che alcune applicazioni verranno scritte per riconoscere le piattaforme note e modificheranno l'utilizzo di OpenGL in base alle caratteristiche note delle prestazioni di queste piattaforme. Le stringhe GL VENDOR e GL RENDERER insieme specificano in modo univoco una piattaforma e non \_ \_ cambieranno da versione a versione. Devono essere usati come tali dagli algoritmi di riconoscimento della piattaforma.

Il formato e il contenuto della stringa restituita **da glGetString** dipendono dall'implementazione, ad eccezione del seguente:

-   I nomi delle estensioni non includeranno spazi e verranno separati da spazi nella stringa GL \_ EXTENSIONS.
-   La stringa \_ GL VERSION inizia con un numero di versione. Il numero di versione usa uno dei formati seguenti:

    *numero \_ principale*. *numero \_ secondario*

    *numero \_ principale*. *numero \_ secondario*. *numero di \_ versione*

-   Le informazioni specifiche del fornitore possono seguire il numero di versione. Il formato dipende dall'implementazione, ma uno spazio separa sempre il numero di versione e le informazioni specifiche del fornitore.
-   Tutte le stringhe hanno terminazione Null.

Se viene generato un errore, **glGetString** restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





