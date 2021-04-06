---
title: attributo represent_as
description: L'attributo \ rappresenta \_ As \ ACF associa un tipo locale denominato nella lingua di destinazione repr-Type con un tipo di trasferimento denominato-type trasferito tra client e server.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- attributo represent_as MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045474"
---
# <a name="represent_as-attribute"></a>rappresenta \_ come attributo

L'attributo **\[ rappresenta \_ come \]** ACF associa un tipo locale denominato nel linguaggio di destinazione *repr-Type* con un tipo di trasferimento *denominato-type* trasferito tra client e server.

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo denominato* 
</dt> <dd>

Specifica il tipo di dati di trasferimento denominato trasferiti tra il client e il server.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica uno o più attributi che si applicano al tipo. Separare più attributi con virgole.

</dd> <dt>

*tipo di repr* 
</dt> <dd>

Specifica il tipo locale rappresentato nella lingua di destinazione presentata alle applicazioni client e server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si usa **\[ rappresenta \_ come \]**, è necessario specificare routine che convertono tra i tipi local e transfer e la memoria libera utilizzata per conservare i dati convertiti. L'attributo **\[ rappresenta \_ come \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.

Il tipo trasferito *denominato-type* deve essere risolto in un tipo di base MIDL, un tipo predefinito o un identificatore di tipo. Per altre informazioni, vedere [tipi di base MIDL](midl-base-types.md).

È necessario specificare le routine seguenti:



| Nome routine                   | Descrizione                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_tipo denominato * * * \_ da \_ locale** | Converte i dati dal tipo locale al tipo di rete. La routine alloca memoria per il tipo di dati di rete, inclusa la memoria per tutti i dati a cui fanno riferimento i puntatori nel tipo di dati di rete.              |
| *\_tipo denominato * * * \_ in \_ locale**   | Converte i dati dal tipo di rete al tipo locale. La routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo locale. RPC alloca memoria per il tipo locale stesso. |
| *\_tipo denominato * * * \_ \_ locale disponibile** | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo locale. RPC libera memoria per il tipo stesso                                                                                             |
| *\_tipo denominato * * * \_ \_ inst libero**  | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo di rete e per il tipo di rete stesso.                                                                                            |



 

Lo stub client chiama ** * * \_ da \_ local** per allocare spazio per il tipo trasmesso e per tradurre i dati dal tipo locale al tipo di rete. Lo stub del server alloca spazio per il tipo di dati originale e chiama il *tipo denominato * * * \_ a \_ local** per tradurre i dati dal tipo di rete al tipo locale.

Al ritorno dal codice dell'applicazione, il client e il server Stub chiamano il *tipo denominato * * * \_ Free \_ inst** per deallocare l'archiviazione per il tipo di rete. Per la deallocazione dell'archiviazione restituita dalla routine, lo stub client chiama il *tipo denominato * * * \_ \_ local libero**.

I tipi seguenti non possono avere un oggetto **\[ rappresentato \_ come \]** attributo:

-   Matrici conformi, variabili o conformi.
-   Strutture in cui l'ultimo membro è una matrice conforme (struttura conforme)
-   Puntatori o tipi che contengono un puntatore
-   Pipe o tipi che contengono pipe
-   Tipi utilizzati come tipo di base per una pipe
-   Handle di tipi [**predefiniti \_ t**](handle-t.md), [**void**](void.md)
-   Tipi con attributo [**\[ handle \]**](handle.md)

## <a name="examples"></a>Esempi

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




