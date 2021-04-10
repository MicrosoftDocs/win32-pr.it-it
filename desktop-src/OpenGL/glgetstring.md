---
title: funzione glGetString (GL. h)
description: La funzione glGetString restituisce una stringa che descrive la connessione OpenGL corrente.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- funzione glGetString OpenGL
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
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964831"
---
# <a name="glgetstring-function"></a>glGetString (funzione)

La funzione **glGetString** restituisce una stringa che descrive la connessione OpenGL corrente.

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
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**\_Fornitore GL**</dt> </dl>             | Restituisce la società responsabile di questa implementazione di OpenGL. Questo nome non viene modificato da release a Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**\_RENDERER GL**</dt> </dl>       | Restituisce il nome del renderer. Questo nome è in genere specifico di una particolare configurazione di una piattaforma hardware. Non cambia da release a Release.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**\_versione GL**</dt> </dl>          | Restituisce una versione o un numero di versione.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**\_estensioni GL**</dt> </dl> | Restituisce un elenco separato da spazi di estensioni supportate per OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *nome* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetString** restituisce un puntatore a una stringa statica che descrive alcuni aspetti della connessione OpenGL corrente.

Poiché OpenGL non include query per le caratteristiche di prestazioni di un'implementazione, si prevede che alcune applicazioni vengano scritte per riconoscere le piattaforme note e modificheranno l'utilizzo di OpenGL in base alle caratteristiche di prestazioni note di queste piattaforme. Il \_ Fornitore di stringhe GL e il \_ RENDERER GL insieme specificano una piattaforma in modo univoco e non cambiano da release a Release. Devono essere usati come tali dagli algoritmi di riconoscimento della piattaforma.

Il formato e il contenuto della stringa restituita da **glGetString** dipendono dall'implementazione, ad eccezione del fatto che:

-   I nomi di estensione non includono spazi e saranno separati da spazi nella stringa di estensioni GL \_ .
-   La \_ stringa di versione di GL inizia con un numero di versione. Il numero di versione usa uno dei seguenti formati:

    *\_ numero principale*. *\_ numero secondario*

    *\_ numero principale*. *\_ numero secondario*. *\_ numero di versione*

-   Le informazioni specifiche del fornitore possono seguire il numero di versione. Il formato dipende dall'implementazione, ma uno spazio separa sempre il numero di versione e le informazioni specifiche del fornitore.
-   Tutte le stringhe hanno terminazione null.

Se viene generato un errore, **glGetString** restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> </dl>

 

 





