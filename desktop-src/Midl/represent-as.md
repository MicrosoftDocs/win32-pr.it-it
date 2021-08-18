---
title: represent_as attributo
description: L'attributo \ represent as\ ACF associa un tipo locale denominato nel repr-type del linguaggio di destinazione a un tipo di trasferimento denominato che viene trasferito \_ tra client e server.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as attributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c76576a7d6710c54573ff78186b3cf6d347afc8c4c242fd6e4c1d49865fb521f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146364"
---
# <a name="represent_as-attribute"></a>rappresentare \_ come attributo

**\[ L'attributo represent \_ as \]** ACF associa un tipo locale denominato nel *repr-type* del linguaggio di destinazione a un tipo di trasferimento *denominato che* viene trasferito tra client e server.

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

*named-type* 
</dt> <dd>

Specifica il tipo di dati di trasferimento denominato trasferito tra client e server.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica uno o più attributi applicabili al tipo. Separare più attributi con virgole.

</dd> <dt>

*repr-type* 
</dt> <dd>

Specifica il tipo locale rappresentato nella lingua di destinazione presentata alle applicazioni client e server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si **\[ usa rappresenta \_ come \]**, è necessario fornire routine che convertono tra i tipi locali e i tipi di trasferimento e la memoria disponibile usata per contenere i dati convertiti. **\[ L'attributo represent \_ as \]** indica agli stub di chiamare le routine di conversione fornite dall'utente.

Il tipo trasferito *denominato-type* deve essere risolto in un tipo di base MIDL, in un tipo predefinito o in un identificatore di tipo. Per altre informazioni, vedere [Tipi di base MIDL.](midl-base-types.md)

È necessario specificare le routine seguenti:



| Nome routine                   | Descrizione                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *tipo \_ denominato*** \_ da \_ locale** | Converte i dati dal tipo locale al tipo di rete. La routine alloca memoria per il tipo di dati di rete, inclusa la memoria per tutti i dati a cui fanno riferimento i puntatori nel tipo di dati di rete.              |
| *tipo \_ denominato*** \_ in \_ locale**   | Converte i dati dal tipo di rete al tipo locale. La routine è responsabile dell'allocazione della memoria per i dati a cui fanno riferimento i puntatori nel tipo locale. RPC alloca memoria per il tipo locale stesso. |
| *tipo \_ denominato*** \_ locale \_ gratuito** | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo locale. RPC libera memoria per il tipo stesso                                                                                             |
| *tipo \_ denominato*** \_ \_ free inst**  | Libera la memoria allocata per i dati a cui fanno riferimento i puntatori nel tipo di rete e per il tipo di rete stesso.                                                                                            |



 

Lo stub client chiama *named-type*** da \_ \_ local** per allocare spazio per il tipo trasmesso e per convertire i dati dal tipo locale al tipo di rete. Lo stub del server alloca spazio per il tipo di dati originale e chiama *named-type*** in \_ \_ local** per convertire i dati dal tipo di rete al tipo locale.

Al ritorno dal codice dell'applicazione, gli stub client e server chiamano *named-type*** \_ \_ free inst** per deallocare l'archiviazione per il tipo di rete. Lo stub client chiama *named-type*** \_ free \_ local** per deallocare l'archiviazione restituita dalla routine.

I tipi seguenti non possono avere un **\[ elemento represent \_ come \]** attributo:

-   Matrici conformi, variabili o variabili conformi
-   Strutture in cui l'ultimo membro è una matrice conforme (struttura conforme)
-   Puntatori o tipi che contengono un puntatore
-   Pipe o tipi che contengono pipe
-   Tipi usati come tipo di base per una pipe
-   I tipi predefiniti [**gestiscono \_ t**](handle-t.md), [**void**](void.md)
-   Tipi con [**\[ l'attributo handle \]**](handle.md)

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

[**Matrici**](arrays-1.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




