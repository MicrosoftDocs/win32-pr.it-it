---
description: Fornisce un modello per la creazione di class factory.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Classe CFactoryTemplate (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f9fbc76fe65e1f1136fb44d22db36500c4d8870f97befa8e36fa08a108ada71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697621"
---
# <a name="cfactorytemplate-class"></a>Classe CFactoryTemplate

Fornisce un modello per la creazione di class factory.

In DirectShow, le class factory sono specializzate usando la **classe CFactoryTemplate,** denominata anche *modello factory*. Ogni class factory contiene un puntatore a un modello di factory. Il modello factory contiene informazioni su un oggetto COM, tra cui l'identificatore di classe (CLSID) dell'oggetto e un puntatore a una funzione che crea l'oggetto.

Nella DLL dichiarare una matrice globale di modelli di factory denominata *g \_ Templates*. Includere un modello factory per ogni oggetto nella DLL. Quando la [**funzione DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuovo class factory, cerca nella matrice un modello con un CLSID corrispondente. Supponendo che ne trovi uno, crea un class factory che contiene un puntatore al modello corrispondente. Quando il client chiama **IClassFactory::CreateInstance,** il class factory chiama la funzione di creazione di istanze definita nel modello.

Per altre informazioni, vedere [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).



| Variabili membro pubbliche                                                   | Descrizione                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ Nome**](cfactorytemplate-m-name.md)                                | Nome del filtro.                                                        |
| [**m \_ ClsID**](cfactorytemplate-m-clsid.md)                              | Puntatore al CLSID dell'oggetto.                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | Puntatore a una funzione che crea un'istanza dell'oggetto .              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.           |
| [**m \_ pAMovieSetup \_ Filter**](cfactorytemplate-m-pamoviesetup-filter.md) | Puntatore a [**una struttura AMOVIESETUP \_ FILTER.**](amoviesetup-filter.md) |
| Metodi pubblici                                                            | Descrizione                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Determina se un CLSID corrisponde a questo modello di classe.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Chiama la funzione di creazione di oggetti per la classe .                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento sulla classe base](base-class-reference.md)
</dt> </dl>

 

